![fd23599e33d52e7a6aba3ab8330a4825.png](../_resources/fd23599e33d52e7a6aba3ab8330a4825.png)

## ！！！！！！！！！

# lecture 5:Language Models and Recurrent Neural Networks

## 1.Language Modeling

- Language Modeling is the task of predicting what word comes next
- 一种定义  
    ![77dba7e9e5033f38306ac2555b38ccd5.png](../_resources/77dba7e9e5033f38306ac2555b38ccd5.png)
- 另一种  
    ![b34d33f9e86d1a11908ea7c1eac1204a.png](../_resources/b34d33f9e86d1a11908ea7c1eac1204a.png)
- n-gram language model  
    ![b18b251a8f4423fb0e841a1b7ebf9159.png](../_resources/b18b251a8f4423fb0e841a1b7ebf9159.png)
    - 马尔可夫假设  
        ![e9fe8222efdfea91ac38543710fb8e7a.png](../_resources/e9fe8222efdfea91ac38543710fb8e7a.png)
    - 稀疏性导致的问题  
        ![6ea4d50555a80e5aba119d497b867db8.png](../_resources/6ea4d50555a80e5aba119d497b867db8.png)
    - 存储问题  
        ![ce02fdaf96a5b781e86c7e111d9f6a45.png](../_resources/ce02fdaf96a5b781e86c7e111d9f6a45.png)
    - 还有可能不同单词之间的概率太过接近
- 评估语言模型：困惑度(perplexity)  
    ![9477ace3ff7c92bd6e930bd00e4b0afe.png](../_resources/9477ace3ff7c92bd6e930bd00e4b0afe.png)

### 建造神经语言模型

- 固定窗口的神经语言模型  
    ![3420d2b3294ff1da6aed74fd033ce0ef.png](../_resources/3420d2b3294ff1da6aed74fd033ce0ef.png)  
    ![1838bddb7348e2fd5c8dc4c4ddbaba99.png](../_resources/1838bddb7348e2fd5c8dc4c4ddbaba99.png)

## 2.recurrent neural networks(RNN)

- core idea:重复应用相同的权重  
    ![7306e993fb5cadd5724671d23cffcc45.png](../_resources/7306e993fb5cadd5724671d23cffcc45.png)  
    ![86f8084ddc21e33f2976ee5212ad2d3a.png](../_resources/86f8084ddc21e33f2976ee5212ad2d3a.png)

### train

![771137bbd3d1f1294d722449ad2b0150.png](../_resources/771137bbd3d1f1294d722449ad2b0150.png)

- teacher forcing:使用原本的输入序列而不是模型上一步的输出作为输入接着算，好处是减少模型初期的误差带来的影响
- ![23addb5ab313113f062ff366b603c877.png](../_resources/23addb5ab313113f062ff366b603c877.png)
- 序列学习：错开一位  
    ![95280d7ba084188bb1f3a65df00b88c1.png](../_resources/95280d7ba084188bb1f3a65df00b88c1.png)

### deep bidirectional rnn

- (注意正向和反向的权重是不一样的)  
    ![b8db8fd0670cdd823a59f6bc992998e4.png](../_resources/b8db8fd0670cdd823a59f6bc992998e4.png)
- 它更为强大，在能获取整个序列的时候应该作为你的默认选择
- 也可以是多层的(multi-layer rnn/stacked rnn)  
    ![3c3e933419b71f407e0d84517c28a8ba.png](../_resources/3c3e933419b71f407e0d84517c28a8ba.png)
- 高效的rnn通常是深层的(但是没有普通的前馈网络和卷积网络那么深)

### 应用：encoder and decoder

![e6a8bc958ef68a196cf2cc5d02dd03ea.png](../_resources/e6a8bc958ef68a196cf2cc5d02dd03ea.png)  
extension to add

1.  训练两套编码器和解码器的权重（要用不同的）
2.  计算decoder使用三个输入（encoder的、上一个时间步的隐状态、上一个时间步的输出）
3.  使用deep(multi-layer)要求使用大语料库
4.  使用双向的rnn  
    5.反过来训练：把梯度消失问题提前处理  
    ![5f07d07099acbfcdab5f7e3738e076d0.png](../_resources/5f07d07099acbfcdab5f7e3738e076d0.png)

## 3.rnn的问题：梯度消失和梯度爆炸

- 梯度链条过长的时候，中间如果有部分很小，梯度会直接消失
- 梯度消失会导致更新仅与较近的文本相关
- 梯度爆炸相对好解决：梯度裁剪
    - ![19f7247a389051f7fa41695bd3975f92.png](../_resources/19f7247a389051f7fa41695bd3975f92.png)
- 梯度消失:LSTM(记忆性)、注意力机制
    - ![0369b0eeb604937e1641f1d20a945a6f.png](../_resources/0369b0eeb604937e1641f1d20a945a6f.png)

## 4.recap

![8a47f00ca5dc8a98d8b3b163df475ee2.png](../_resources/8a47f00ca5dc8a98d8b3b163df475ee2.png)

## words

recap:概述  
benchmark:基准、评估  
Cygwin:小型的linux模拟环境  
Stylistically:在文体上  
discard：扔出、弃置  
granularity：间隔  
incoherent：语无伦次，不合逻辑  
truncated：缩短的，截去顶端的  
eigenvalues ：特征值  
decouples 分离

# lecture 6:LSTM RNNs and Neural Machine Translation

- rnn!=language model(后者还可以运用在别的地方)

## 1.Long Short-Term Memory RNNs (LSTMs)

![35481118335faa7ffbb20af1c17dcfb4.png](../_resources/35481118335faa7ffbb20af1c17dcfb4.png)  
可视化  
![55eff6f399dd95977bf411a4b12db303.png](../_resources/55eff6f399dd95977bf411a4b12db303.png)

## 2.其他方案

- 梯度消失或爆炸并不只是rnn的问题，一般的前馈、卷积神经网络也有（梯度链子太长）
- 一种方案就是建立更直接的联系（跳过中间层，直接把梯度传过去（残差网络））、也叫skip-connection  
    ![494f30aabc889a7d9ab84696cfa9581b.png](../_resources/494f30aabc889a7d9ab84696cfa9581b.png)
- 另一种：使用dense layer、highwayNet  
    ![e84cbcd7cf68e63923fbada85b96b9b1.png](../_resources/e84cbcd7cf68e63923fbada85b96b9b1.png)  
    **!注意区分：densenet和denselayer**  
    前者是每一层输出连接又输进去，是为了解决梯度路径的问题，后者就是全连接层的别称

## 3.machine translation

### 统计方法（statistical machine translation）

![dc90b903f220e7c98db1cba951c175af.png](../_resources/dc90b903f220e7c98db1cba951c175af.png)

### NMT(neural)

seq2seq  
![66abec7fc9eaa0deadc1c9ddc0046c47.png](../_resources/66abec7fc9eaa0deadc1c9ddc0046c47.png)  
其优化是作为一整个来搞的  
![3eba9dfa7b9980e8ab5299815fe67416.png](../_resources/3eba9dfa7b9980e8ab5299815fe67416.png)

## 4.problem and solution

1.仍然较难以捕捉长期关系  
2.并行做的不好：后面的隐藏层没办法算，在前面的隐状态算完之前

### solution:attention

**Attention is just a weighted average – this is very powerful if the weights are learned!**

#### attention in seq2seq

![03de738dcb1f99b7294b39f18e6fe67f.png](../_resources/03de738dcb1f99b7294b39f18e6fe67f.png)  
![05691b8100be9edcbafb24514c5f5616.png](../_resources/05691b8100be9edcbafb24514c5f5616.png)  
attention in equation  
![a58be405747f5712f7f7ecbb5187972c.png](../_resources/a58be405747f5712f7f7ecbb5187972c.png)

#### 更一般的定义

注意力就是给定值（一组向量），查询（一个向量），基于查询给出值的加权和

## 5.总结

![19d4ae21a8e243e850597d79b8ec7519.png](../_resources/19d4ae21a8e243e850597d79b8ec7519.png)

## arxiv:收录论文预印版的网站

## words

lag：掉队、时间间隔  
vanilla ：香草、普通的  
feed-forward 前馈神经网络  
empirical：经验的  
unimpeded:畅通无阻的  
diagram:图  
depict:描述、描绘  
concurrent:同时发生的、一致的  
fidelity:忠诚、精确度  
fringe:次要的、非主流的  
bottleneck：瓶颈  
alignment:结盟、协调一致
tokenizer：分词器
morpheme:语素
tweaking:稍作调整
hypotheses：假定、臆测
# assignment 3

func1

```python
def pad_sents(sents, pad_token):
    """ Pad list of sentences according to the longest sentence in the batch.
        The paddings should be at the end of each sentence.
    @param sents (list[list[str]]): list of sentences, where each sentence
                                    is represented as a list of words
    @param pad_token (str): padding token
    @returns sents_padded (list[list[str]]): list of sentences where sentences shorter
        than the max length sentence are padded out with the pad_token, such that
        each sentences in the batch now has equal length.
    """
    sents_padded = []

    ### YOUR CODE HERE (~6 Lines)
    max_length=-1
    for sentense in sents:
        max_length=len(sentense) if max_length<len(sentense) else max_length
    for sentense in sents:
        sents_padded.append(sentense+(max_length-len(sentense))*[pad_token])#注意一个句子是list[str]类型，添加的填充词汇应该是以重复列表的形式加进去
    ### END YOUR CODE

    return sents_padded
```

func2:

```python
     def encode(self, source_padded: torch.Tensor, source_lengths: List[int], grader_params=None) -> Tuple[
        torch.Tensor, Tuple[torch.Tensor, torch.Tensor]]:
        """ Apply the encoder to source sentences to obtain encoder hidden states.
            Additionally, take the final states of the encoder and project them to obtain initial states for decoder.

        @param source_padded (Tensor): Tensor of padded source sentences with shape (src_len, b), where
                                        b = batch_size, src_len = maximum source sentence length. Note that
                                       these have already been sorted in order of longest to shortest sentence.
        @param source_lengths (List[int]): List of actual lengths for each of the source sentences in the batch
        @returns enc_hiddens (Tensor): Tensor of hidden units with shape (b, src_len, h*2), where
                                        b = batch size, src_len = maximum source sentence length, h = hidden size.
        @returns dec_init_state (tuple(Tensor, Tensor)): Tuple of tensors representing the decoder's initial
                                                hidden state and cell.
        @grader_params: Ignore this parameter. It is used for grading purposes.
        """
        enc_hiddens, dec_init_state = None, None

        ### YOUR CODE HERE (~ 11 Lines)
        X=self.model_embeddings.source(source_padded)#应该直接调用其source方法而不是直接将整个类作为函数调用，否则会触发默认调用forward方法
        x=torch.permute(self.post_embed_cnn(torch.permute(X,(1,2,0))),(2,0,1))
        x_i =nn.utils.rnn.pack_padded_sequence(x,lengths=source_lengths,batch_first=False)#！打包序列 (注意batch_first=False因为输入是src_len第一维)
        enc,(last_hidden,last_cell)=self.encoder(x_i)#对双向网络而言，其返回隐状态包含了正向和反向
        enc_h,_=nn.utils.rnn.pad_packed_sequence(enc,batch_first=False)
        enc_hiddens=torch.permute(enc_h,(1,0,2))
        init_decoder_hidden=self.h_projection(torch.cat((last_hidden[0],last_hidden[1]),dim=1))#正确处理，正反向正确拼接
        init_decoder_cell=self.c_projection(torch.cat((last_cell[0],last_cell[1]),dim=1))
        dec_init_state=(init_decoder_hidden,init_decoder_cell)#解码器需要的就是元组
        ### TODO:
        ###     1. Construct Tensor `X` of source sentences with shape (src_len, b, e) using the source model embeddings.
        ###         src_len = maximum source sentence length, b = batch size, e = embedding size. Note
        ###         that there is no initial hidden state or cell for the encoder.
        ###     2. Apply the post_embed_cnn layer. Before feeding X into the CNN, first use torch.permute to change the
        ###         shape of X to (b, e, src_len). After getting the output from the CNN, remember to use torch.permute
        ###         again to revert X back to its original shape.
        ###     3. Compute `enc_hiddens`, `last_hidden`, `last_cell` by applying the encoder to `X`.
        ###         - Before you can apply the encoder, you need to apply the `pack_padded_sequence` function to X.
        ###         - After you apply the encoder, you need to apply the `pad_packed_sequence` function to enc_hiddens.
        ###         - Note that the shape of the tensor returned by the encoder is (src_len, b, h*2) and we want to
        ###           return a tensor of shape (b, src_len, h*2) as `enc_hiddens`.
        ###     4. Compute `dec_init_state` = (init_decoder_hidden, init_decoder_cell):
        ###         - `init_decoder_hidden`:
        ###             `last_hidden` is a tensor shape (2, b, h). The first dimension corresponds to forwards and backwards.
        ###             Concatenate the forwards and backwards tensors to obtain a tensor shape (b, 2*h).
        ###             Apply the h_projection layer to this in order to compute init_decoder_hidden.
        ###             This is h_0^{dec} in the PDF. Here b = batch size, h = hidden size
        ###         - `init_decoder_cell`:
        ###             `last_cell` is a tensor shape (2, b, h). The first dimension corresponds to forwards and backwards.
        ###             Concatenate the forwards and backwards tensors to obtain a tensor shape (b, 2*h).
        ###             Apply the c_projection layer to this in order to compute init_decoder_cell.
        ###             This is c_0^{dec} in the PDF. Here b = batch size, h = hidden size
        ###
        ### See the following docs, as you may need to use some of the following functions in your implementation:
        ###     Pack the padded sequence X before passing to the encoder:
        ###         https://pytorch.org/docs/stable/generated/torch.nn.utils.rnn.pack_padded_sequence.html
        ###     Pad the packed sequence, enc_hiddens, returned by the encoder:
        ###         https://pytorch.org/docs/stable/generated/torch.nn.utils.rnn.pad_packed_sequence.html
        ###     Tensor Concatenation:
        ###         https://pytorch.org/docs/stable/generated/torch.cat.html
        ###     Tensor Permute:
        ###         https://pytorch.org/docs/stable/generated/torch.permute.html







        ### END YOUR CODE

        return enc_hiddens, dec_init_state
```

func3

```python
    def __init__(self, embed_size, hidden_size, vocab, dropout_rate=0.2):
        """ Init NMT Model.

        @param embed_size (int): Embedding size (dimensionality)
        @param hidden_size (int): Hidden Size, the size of hidden states (dimensionality)
        @param vocab (Vocab): Vocabulary object containing src and tgt languages
                              See vocab.py for documentation.
        @param dropout_rate (float): Dropout probability, for attention
        """
        super(NMT, self).__init__()
        self.model_embeddings = ModelEmbeddings(embed_size, vocab)
        self.hidden_size = hidden_size
        self.dropout_rate = dropout_rate
        self.vocab = vocab

        # default values
        self.post_embed_cnn = None
        self.encoder = None
        self.decoder = None
        self.h_projection = None
        self.c_projection = None
        self.att_projection = None
        self.combined_output_projection = None
        self.target_vocab_projection = None
        self.dropout = None
        # For sanity check only, not relevant to implementation
        self.gen_sanity_check = False
        self.counter = 0

        ### YOUR CODE HERE (~9 Lines)
        self.post_embed_cnn=nn.Conv1d(embed_size,embed_size,kernel_size=2,padding="same")
        #卷积层！不是设定input和output就完事！！！动态填充，确保一定能够是完全相同的形状
        #看看计算对不对
        self.encoder=nn.LSTM(embed_size,self.hidden_size,bidirectional=True)
        self.decoder=nn.LSTMCell(embed_size+self.hidden_size,self.hidden_size,bias=True)
        self.h_projection=nn.Linear(2*self.hidden_size,self.hidden_size,bias=False)#2在前面
        self.c_projection=nn.Linear(2*self.hidden_size,self.hidden_size,bias=False)
        self.att_projection=nn.Linear(2*self.hidden_size,self.hidden_size,bias=False)
        self.combined_output_projection=nn.Linear(3*self.hidden_size,self.hidden_size,bias=False)
        self.target_vocab_projection=nn.Linear(self.hidden_size,len(self.vocab.tgt),bias=False)#从隐藏映射出去
        self.dropout=nn.Dropout(self.dropout_rate)
        ### TODO - Initialize the following variables IN THIS ORDER:
        ###     self.post_embed_cnn (Conv1d layer with kernel size 2, input and output channels = embed_size,
        ###         padding = same to preserve output shape )
        ###     self.encoder (Bidirectional LSTM with bias)
        ###     self.decoder (LSTM Cell with bias)
        ###     self.h_projection (Linear Layer with no bias), called W_{h} in the PDF.
        ###     self.c_projection (Linear Layer with no bias), called W_{c} in the PDF.
        ###     self.att_projection (Linear Layer with no bias), called W_{attProj} in the PDF.
        ###     self.combined_output_projection (Linear Layer with no bias), called W_{u} in the PDF.
        ###     self.target_vocab_projection (Linear Layer with no bias), called W_{vocab} in the PDF.
        ###     self.dropout (Dropout Layer)
        ###
        ### Use the following docs to properly initialize these variables:
        ###     Conv1d:
        ###         https://pytorch.org/docs/stable/generated/torch.nn.Conv1d.html
        ###     LSTM:
        ###         https://pytorch.org/docs/stable/generated/torch.nn.LSTM.html
        ###     LSTM Cell:
        ###         https://pytorch.org/docs/stable/generated/torch.nn.LSTMCell.html
        ###     Linear Layer:
        ###         https://pytorch.org/docs/stable/generated/torch.nn.Linear.html
        ###     Dropout Layer:
        ###         https://pytorch.org/docs/stable/generated/torch.nn.Dropout.html



        ### END YOUR CODE
```

func4

```python
    def decode(self, enc_hiddens: torch.Tensor, enc_masks: torch.Tensor,
               dec_init_state: Tuple[torch.Tensor, torch.Tensor], target_padded: torch.Tensor) -> torch.Tensor:
        """Compute combined output vectors for a batch.

        @param enc_hiddens (Tensor): Hidden states (b, src_len, h*2), where
                                     b = batch size, src_len = maximum source sentence length, h = hidden size.
        @param enc_masks (Tensor): Tensor of sentence masks (b, src_len), where
                                     b = batch size, src_len = maximum source sentence length.
        @param dec_init_state (tuple(Tensor, Tensor)): Initial state and cell for decoder
        @param target_padded (Tensor): Gold-standard padded target sentences (tgt_len, b), where
                                       tgt_len = maximum target sentence length, b = batch size.

        @returns combined_outputs (Tensor): combined output tensor  (tgt_len, b,  h), where
                                        tgt_len = maximum target sentence length, b = batch_size,  h = hidden size
        """
        # Chop off the <END> token for max length sentences.
        target_padded = target_padded[:-1]

        # Initialize the decoder state (hidden and cell)
        dec_state = dec_init_state

        # Initialize previous combined output vector o_{t-1} as zero
        batch_size = enc_hiddens.size(0)
        o_prev = torch.zeros(batch_size, self.hidden_size, device=self.device)

        # Initialize a list we will use to collect the combined output o_t on each step
        combined_outputs = []

        ### YOUR CODE HERE (~9 Lines)
        enc_hiddens_proj=self.att_projection(enc_hiddens)
        Y=self.model_embeddings.target(target_padded)
        for Y_t in torch.split(Y,1):#默认从dim=0切
            Y_t=torch.squeeze(Y_t)#默认把长度为1的去掉了
            Ybar_t=torch.cat((Y_t,o_prev),dim=-1)
            dec_state,output,e_t=self.step(Ybar_t, dec_state, enc_hiddens, enc_hiddens_proj, enc_masks)
            combined_outputs.append(output)
            o_prev=output
        combined_outputs=torch.stack(combined_outputs,dim=0)
        ### TODO:
        ###     1. Apply the attention projection layer to `enc_hiddens` to obtain `enc_hiddens_proj`,
        ###         which should be shape (b, src_len, h),
        ###         where b = batch size, src_len = maximum source length, h = hidden size.
        ###         This is applying W_{attProj} to h^enc, as described in the PDF.
        ###     2. Construct tensor `Y` of target sentences with shape (tgt_len, b, e) using the target model embeddings.
        ###         where tgt_len = maximum target sentence length, b = batch size, e = embedding size.
        ###     3. Use the torch.split function to iterate over the time dimension of Y.
        ###         Within the loop, this will give you Y_t of shape (1, b, e) where b = batch size, e = embedding size.
        ###             - Squeeze Y_t into a tensor of dimension (b, e).
        ###             - Construct Ybar_t by concatenating Y_t with o_prev on their last dimension
        ###             - Use the step function to compute the the Decoder's next (cell, state) values
        ###               as well as the new combined output o_t.
        ###             - Append o_t to combined_outputs
        ###             - Update o_prev to the new o_t.
        ###     4. Use torch.stack to convert combined_outputs from a list length tgt_len of
        ###         tensors shape (b, h), to a single tensor shape (tgt_len, b, h)
        ###         where tgt_len = maximum target sentence length, b = batch size, h = hidden size.
        ###
        ### Note:
        ###    - When using the squeeze() function make sure to specify the dimension you want to squeeze
        ###      over. Otherwise, you will remove the batch dimension accidentally, if batch_size = 1.
        ###
        ### You may find some of these functions useful:
        ###     Zeros Tensor:
        ###         https://pytorch.org/docs/stable/generated/torch.zeros.html
        ###     Tensor Splitting (iteration):
        ###         https://pytorch.org/docs/stable/generated/torch.split.html
        ###     Tensor Dimension Squeezing:
        ###         https://pytorch.org/docs/stable/generated/torch.squeeze.html
        ###     Tensor Concatenation:
        ###         https://pytorch.org/docs/stable/generated/torch.cat.html
        ###     Tensor Stacking:
        ###         https://pytorch.org/docs/stable/generated/torch.stack.html






        ### END YOUR CODE

        return combined_outputs
```

func5

```python
    def step(self, Ybar_t: torch.Tensor,
             dec_state: Tuple[torch.Tensor, torch.Tensor],
             enc_hiddens: torch.Tensor,
             enc_hiddens_proj: torch.Tensor,
             enc_masks: torch.Tensor) -> Tuple[Tuple, torch.Tensor, torch.Tensor]:
        """ Compute one forward step of the LSTM decoder, including the attention computation.

        @param Ybar_t (Tensor): Concatenated Tensor of [Y_t o_prev], with shape (b, e + h). The input for the decoder,
                                where b = batch size, e = embedding size, h = hidden size.
        @param dec_state (tuple(Tensor, Tensor)): Tuple of tensors both with shape (b, h), where b = batch size, h = hidden size.
                First tensor is decoder's prev hidden state, second tensor is decoder's prev cell.
        @param enc_hiddens (Tensor): Encoder hidden states Tensor, with shape (b, src_len, h * 2), where b = batch size,
                                    src_len = maximum source length, h = hidden size.
        @param enc_hiddens_proj (Tensor): Encoder hidden states Tensor, projected from (h * 2) to h. Tensor is with shape (b, src_len, h),
                                    where b = batch size, src_len = maximum source length, h = hidden size.
        @param enc_masks (Tensor): Tensor of sentence masks shape (b, src_len),
                                    where b = batch size, src_len is maximum source length.

        @returns dec_state (tuple (Tensor, Tensor)): Tuple of tensors both shape (b, h), where b = batch size, h = hidden size.
                First tensor is decoder's new hidden state, second tensor is decoder's new cell.
        @returns combined_output (Tensor): Combined output Tensor at timestep t, shape (b, h), where b = batch size, h = hidden size.
        @returns e_t (Tensor): Tensor of shape (b, src_len). It is attention scores distribution.
                                Note: You will not use this outside of this function.
                                      We are simply returning this value so that we can sanity check
                                      your implementation.
        """

        combined_output = None

        ### YOUR CODE HERE (~3 Lines)
        dec_state=self.decoder(Ybar_t,dec_state)
        dec_hidden,dec_cell=dec_state[0],dec_state[1]
        e_t=torch.squeeze(torch.bmm(torch.unsqueeze(dec_hidden,dim=1),torch.permute(enc_hiddens_proj,(0,2,1))),dim=1)
        #squeeze还是指定维度更好
        #理解：enc_hiddens_proj是投影过后的hidden
        ### TODO:
        ###     1. Apply the decoder to `Ybar_t` and `dec_state`to obtain the new dec_state.
        ###     2. Split dec_state into its two parts (dec_hidden, dec_cell)
        ###     3. Compute the attention scores e_t, a Tensor shape (b, src_len).
        ###        Note: b = batch_size, src_len = maximum source length, h = hidden size.
        ###
        ###       Hints:
        ###         - dec_hidden is shape (b, h) and corresponds to h^dec_t in the PDF (batched)
        ###         - enc_hiddens_proj is shape (b, src_len, h) and corresponds to W_{attProj} h^enc (batched).
        ###         - Use batched matrix multiplication (torch.bmm) to compute e_t (be careful about the input/ output shapes!)
        ###         - To get the tensors into the right shapes for bmm, you will need to do some squeezing and unsqueezing.
        ###         - When using the squeeze() function make sure to specify the dimension you want to squeeze
        ###             over. Otherwise, you will remove the batch dimension accidentally, if batch_size = 1.
        ###
        ### Use the following docs to implement this functionality:
        ###     Batch Multiplication:
        ###         https://pytorch.org/docs/stable/generated/torch.bmm.html
        ###     Tensor Unsqueeze:
        ###         https://pytorch.org/docs/stable/generated/torch.unsqueeze.html
        ###     Tensor Squeeze:
        ###         https://pytorch.org/docs/stable/generated/torch.squeeze.html


        ### END YOUR CODE

        # Set e_t to -inf where enc_masks has 1
        if enc_masks is not None:
            e_t.data.masked_fill_(enc_masks.bool(), -float('inf'))

        ### YOUR CODE HERE (~6 Lines)
        alpha_t=F.softmax(e_t,dim=1)
        a_t=torch.squeeze(torch.bmm(torch.unsqueeze(alpha_t,dim=1),enc_hiddens),dim=1)
        U_t=torch.cat((dec_hidden,a_t),dim=1)
        #torch.cat:dim设置的哪个，哪个dim的值就变大（简记）
        V_t=self.combined_output_projection(U_t)
        O_t=self.dropout(torch.tanh(V_t))
        ### TODO:
        ###     1. Apply softmax to e_t to yield alpha_t
        ###     2. Use batched matrix multiplication between alpha_t and enc_hiddens to obtain the
        ###         attention output vector, a_t.
        ###           - alpha_t is shape (b, src_len)
        ###           - enc_hiddens is shape (b, src_len, 2h)
        ###           - a_t should be shape (b, 2h)
        ###           - You will need to do some squeezing and unsqueezing.
        ###     Note: b = batch size, src_len = maximum source length, h = hidden size.
        ###
        ###     3. Concatenate dec_hidden with a_t to compute tensor U_t
        ###     4. Apply the combined output projection layer to U_t to compute tensor V_t
        ###     5. Compute tensor O_t by first applying the Tanh function and then the dropout layer.
        ###
        ### Use the following docs to implement this functionality:
        ###     Softmax:
        ###         https://pytorch.org/docs/stable/generated/torch.nn.functional.softmax.html
        ###     Batch Multiplication:
        ###         https://pytorch.org/docs/stable/generated/torch.bmm.html
        ###     Tensor View:
        ###         https://pytorch.org/docs/stable/generated/torch.Tensor.view.html
        ###     Tensor Concatenation:
        ###         https://pytorch.org/docs/stable/generated/torch.cat.html
        ###     Tanh:
        ###         https://pytorch.org/docs/stable/generated/torch.tanh.html


        ### END YOUR CODE

        combined_output = O_t
        return dec_state, combined_output, e_t
```

## 三种注意力

![2722b09209804ede9fd130b9ab5dd346.png](../_resources/2722b09209804ede9fd130b9ab5dd346.png)

![f5f19b24feaf000568da8ebe075a4d5a.png](../_resources/f5f19b24feaf000568da8ebe075a4d5a.png)

# ！torch.squeeze()

其默认把长度为1的都木大了，最好每次用的时候指定维度！！！！  
使用自定义类型的时候  
在load时注意weight_only=False(一种粗暴解决方案)  
跑.sh文件(注意传参数)

在 Linux/macOS 或 Windows 上运行 `.sh` (Shell 脚本) 文件的方法如下：

* * *

### **1\. Linux/macOS 运行方法**

#### **（1）添加执行权限**

默认情况下，`.sh` 文件可能没有执行权限，需先运行：

```bash
chmod +x your_script.sh  # 赋予可执行权限
```

#### **（2）运行脚本**

```bash
./your_script.sh        # 直接运行（需在脚本所在目录）
```

或

```bash
bash your_script.sh     # 显式指定用 bash 执行（无需权限）
```

#### **（3）调试脚本**

```bash
bash -x your_script.sh  # 打印每条执行的命令（调试用）
```

* * *

### **2\. Windows 运行方法**

Windows 默认不支持直接运行 `.sh` 文件，需以下方式：

#### **（1）使用 Git Bash / WSL (推荐)**

- 安装 [Git for Windows](https://gitforwindows.org/) 或 [WSL](https://learn.microsoft.com/en-us/windows/wsl/install)，然后在终端中按 **Linux 方式**运行。

#### **（2）使用 Cygwin**

安装 Cygwin 后，在它的终端中运行 `.sh` 文件。

#### **（3）通过 Docker**

如果脚本是 Linux 环境专用，可以在 Windows Docker 容器中运行。

* * *

### **3\. 常见问题**

#### **错误：`Permission denied`**

```bash
chmod +x your_script.sh  # 确保已添加执行权限
```

#### **错误：`/bin/bash^M: bad interpreter`**

脚本文件的行尾符是 Windows 格式（`\r\n`），需转换为 Unix 格式（`\n`）：

```bash
sed -i 's/\r$//' your_script.sh  # 在 Linux/macOS 修复
```

或使用 `dos2unix` 工具：

```bash
dos2unix your_script.sh
```

#### **脚本需要参数**

如果脚本需要输入参数（如 `run.sh train --lr=0.1`），直接附加在命令后：

```bash
./run.sh train --lr=0.1
```

* * *

### **4\. 示例**

假设有一个 `train.sh`：

```bash
#!/bin/bash
echo "Training model with GPU..."
python run.py train --cuda --batch-size=64
```

运行步骤：

```bash
chmod +x train.sh  # 加权限
./train.sh         # 执行
```

* * *

### **总结**

| 系统  | 方法  | 备注  |
| --- | --- | --- |
| **Linux/macOS** | `chmod +x` + `./script.sh` | 需权限 |
| **Windows** | Git Bash / WSL / Cygwin | 需安装兼容环境 |

**较新的ubuntu发行版中只有python3而没有python，写脚本要换**
## writing
### improvement
1.加入单复数检测模块
- 数据标记时直接加入单复数标记
- 利用数据单独训练一个子单复数分类器

2.政治类翻译问题
- 构建术语表强制对齐
- 采用领域自适应（Domain Adaptation）：使用该领域语料混合训练、显式引入领域标签、对抗训练

3.谚语问题
- 构建谚语库，直接训练
- 检索增强生成（RAG）：结合信息检索和文本生成，通过检索器和生成器联合训练。

4.并列结构
- 采用并列数据训练

### BLEU
### **BLEU分数计算示例**
![5e1258ba5d264c5681aa2a44c7895ef7.png](../_resources/5e1258ba5d264c5681aa2a44c7895ef7.png)
BLEU（Bilingual Evaluation Understudy）是一种用于评估机器翻译质量的自动指标，通过比较机器翻译（**候选文本**）与人工参考翻译（**参考文本**）的相似性来打分。其核心思想是统计**n-gram（连续n个词）的重合程度**，并结合句子长度的惩罚机制。

---

#### **1. 基础概念**
- **n-gram精度（Precision）**：  
  统计候选翻译中所有n-gram在参考翻译中出现的比例。  
  - 例如，1-gram（单词级别）、2-gram（短语级别）等。  
- **长度惩罚（Brevity Penalty, BP）**：  
  防止过短的候选翻译因高n-gram精度得分虚高。

---

#### **2. 计算步骤（通过示例说明）**
**候选翻译（Candidate）**：`the cat is on the mat`  
**参考翻译（Reference）**：`the cat is sitting on the mat`  

##### **Step 1: 计算n-gram精度**
- **1-gram（单词）**：  
  - 候选翻译的1-gram：`the, cat, is, on, the, mat`（共6个词）。  
  - 在参考翻译中出现的词：`the`（2次）、`cat`（1次）、`is`（1次）、`on`（1次）、`mat`（1次）。  
  - **匹配次数**：`the`（最多匹配2次）、`cat`（1次）、`is`（1次）、`on`（1次）、`mat`（1次） → 总计匹配6次。  
  - **精度** = 匹配数 / 候选总词数 = 6/6 = 1.0。  

- **2-gram（短语）**：  
  - 候选翻译的2-gram：`the cat, cat is, is on, on the, the mat`（共5个）。  
  - 参考翻译的2-gram：`the cat, cat is, is sitting, sitting on, on the, the mat`。  
  - **匹配的2-gram**：`the cat, cat is, on the, the mat` → 共4个。  
  - **精度** = 4/5 = 0.8。  

（同理可计算3-gram、4-gram精度，此处省略）

##### **Step 2: 综合n-gram精度**
假设我们计算到4-gram，各n-gram精度为：  
- \( p_1 = 1.0 \), \( p_2 = 0.8 \), \( p_3 = 0.6 \), \( p_4 = 0.5 \)  
- **几何平均**：  
 $\text{BP} \cdot \exp\left(\sum_{n=1}^4 w_n \log p_n\right), \quad \text{通常} \ w_n = \frac{1}{4}$

##### **Step 3: 长度惩罚（BP）**
选择与候选翻译长度最接近的，（两个同样接近的话选短的那个）
- 候选翻译长度（c = 6），参考翻译长度（r = 7 ）。  
- 若 $c \leq r$，$BP= e^{1 - r/c}= e^{1 - 7/6} \approx 0.81$。  
- 若 c > r，BP = 1（不惩罚）。  

##### **Step 4: 最终BLEU分数**

$\text{BLEU} = 0.81 \cdot \exp\left(0.25 \cdot \log 1.0 + 0.25 \cdot \log 0.8 + 0.25 \cdot \log 0.6 + 0.25 \cdot \log 0.5\right) \approx 0.73$


---

#### **3. 实际简化计算**
实际工具（如NLTK）会自动化上述过程。以下是Python示例：
```python
from nltk.translate.bleu_score import sentence_bleu
reference = [['the', 'cat', 'is', 'sitting', 'on', 'the', 'mat']]
candidate = ['the', 'cat', 'is', 'on', 'the', 'mat']
score = sentence_bleu(reference, candidate, weights=(0.25, 0.25, 0.25, 0.25))
print(score)  # 输出约0.73
```

---

#### **4. 关键注意事项**
1. **多参考翻译**：  
   若有多个参考翻译，BLEU会取各n-gram匹配的最大值（更公平）。  
2. **n-gram权重**：  
   通常4-gram权重均等（0.25），但可根据任务调整（如更看重1-gram）。  
3. **局限性**：  
   - 不关注语义，仅统计表面匹配。  
   - 对短句严格（长度惩罚可能过重）。  

---

#### **5. 极端案例**
- **候选与参考完全一致**：BLEU=1.0。  
- **候选无任何匹配**：BLEU=0.0。  
- **候选过短**：如`the the the`，1-gram精度高但因BP惩罚得分低。  

通过这种量化方式，BLEU为机器翻译提供了一种快速、可复现的评估手段。

