# unit1 Probability counting and story proof
## 1.2
![8b0a2e7533e6690f9e1d56f29ae923ee.png](../_resources/8b0a2e7533e6690f9e1d56f29ae923ee.png)
- 样本空间可有限可无限，有限就可以变成pebble world
	- 这种情况下做实验等价于从peddles中随机采样
	- Each pebble represents an outcome, and an event is a set of pebbles
### dictionary of set theory
![02fa795e1d3946e31e92ac8accfdc466.png](../_resources/02fa795e1d3946e31e92ac8accfdc466.png)
![fc021ee0d20b603c67c838760ba46fad.png](../_resources/fc021ee0d20b603c67c838760ba46fad.png)
- 德摩根定律：交集的补集=补集的并集
## 1.3
![bd3a9a9aa10b5e854693769a680711e5.png](../_resources/bd3a9a9aa10b5e854693769a680711e5.png)
- restrictions:等可能并且样本空间有限
## 1.4
- 乘法原则
![341119eeb351183703574593e421a798.png](../_resources/341119eeb351183703574593e421a798.png)
![5edaaa0eee1b727423c92c837b32cd71.png](../_resources/5edaaa0eee1b727423c92c837b32cd71.png)
![fcc43e658b3885575ecbf869f1a702bc.png](../_resources/fcc43e658b3885575ecbf869f1a702bc.png)
![4cb7c085779b005b052437b7cbf88382.png](../_resources/4cb7c085779b005b052437b7cbf88382.png)
![d52c4a163b709c9b1873e529ef76b9b9.png](../_resources/d52c4a163b709c9b1873e529ef76b9b9.png)
## 1.5 story proof
![65d596d92b89951c540a22ad05da7cb9.png](../_resources/65d596d92b89951c540a22ad05da7cb9.png)
![6c80fab71f11becb021f17adc9bcc633.png](../_resources/6c80fab71f11becb021f17adc9bcc633.png)
## 1.6
general definition
![16dad4952f69775880cf13a36b7eb0d7.png](../_resources/16dad4952f69775880cf13a36b7eb0d7.png)
- 关于概率函数:
	- 1.频率观点：认为概率表示一种在大量重复实验条件下的长期频率
	- 2.贝叶斯观点：对所讨论事件的信任程度
![3c37a5a1e8737a9b87d43fe99f2ea102.png](../_resources/3c37a5a1e8737a9b87d43fe99f2ea102.png)
![d25496a19807ba01a5063436fe568ea6.png](../_resources/d25496a19807ba01a5063436fe568ea6.png)
![2616ab4a1e6f54bcb0a150329cba71cd.png](../_resources/2616ab4a1e6f54bcb0a150329cba71cd.png)
![45dbbb49288abae9710a671fc8bba9d0.png](../_resources/45dbbb49288abae9710a671fc8bba9d0.png)
## work
![767ce26d6afc32bf93e57a5980b3fd3b.png](../_resources/767ce26d6afc32bf93e57a5980b3fd3b.png)
## word
axiom:公理
factorial:阶乘
unions, intersections, and complements:并集、交集、补集

# unit2 conditional probability and baye's rule
## 2.1
- conditioning:the soul
	- In fact, a useful perspective is that all probabilities are conditional; whether or not it's written explicitly, there is always background knowledge (or assumptions) built into every probability.
## 2.2
- ''prior" means before updating based on the evidence, and ''posterior" means after updating based on the evidence
- 检察官谬误（prosecutor's fallacy）是一种非形式谬误，系取一不甚相关、或有关但未正确考虑条件几率的数据，认定被告“无辜的几率”很小。
## 2.3
- 贝叶斯
![0f41dfb5f75bf8de8726de5f0ecb93fe.png](../_resources/0f41dfb5f75bf8de8726de5f0ecb93fe.png)
- 全概率
![3c1e0302e754d62156dd21916ebd9fea.png](../_resources/3c1e0302e754d62156dd21916ebd9fea.png)
## 2.4
- 条件概率仍然是概率:即所有的概率相关性质对条件概率仍成立
![09efd9e3d990bf6483978cc76b795571.png](../_resources/09efd9e3d990bf6483978cc76b795571.png)
## 2.5
![3b20945cec121fadda87839a2e45a780.png](../_resources/3b20945cec121fadda87839a2e45a780.png)
- 独立性具有对称关系
- 独立和互斥之间的关系:互斥肯定是不独立的，两者不是一个概念
- 推广到三者以上时
![7ac31ff6406af55750f6ecff08875c7c.png](../_resources/7ac31ff6406af55750f6ecff08875c7c.png)
- 条件独立
- ![de761eded64de00440edc5b82d9412bd.png](../_resources/de761eded64de00440edc5b82d9412bd.png)
- conditional independence doesn't imply independence
- independence doesn't imply conditional independence
## 2.6
- condition is a powerful strategy(condition on what you want to know)
- e.g:著名反直觉问题
![ca7f0a3ae7e809611a2bfa150cbd46a8.png](../_resources/ca7f0a3ae7e809611a2bfa150cbd46a8.png)
e.g:条件策略
![3f3cada0a2e4339f554116857e8560d2.png](../_resources/3f3cada0a2e4339f554116857e8560d2.png)
![1d2dabb544b1a8678fdaed5a77a17673.png](../_resources/1d2dabb544b1a8678fdaed5a77a17673.png)
- 辛普森悖论（英语：Simpson's paradox），是概率和统计中的一种现象，其中趋势出现在几组数据中，但当这些组被合并后趋势消失或反转。
## work
![2ad5a319cb6241ebbee1950d89c39293.png](../_resources/2ad5a319cb6241ebbee1950d89c39293.png)
什么是条件就对着什么拆

## word
tandem:串联
chronological:按时间顺序
exacerbate:加剧
contestant:参赛者
# unit3 discrete random variables
## 3.1
![0855cf39ce11cb26664c02c0fc88316a.png](../_resources/0855cf39ce11cb26664c02c0fc88316a.png)
- e.g:扔两次硬币的实验，设x为头向上的数量，x(HH)=2;
## 3.2
![65503482ee411169d0583bbf6daa5323.png](../_resources/65503482ee411169d0583bbf6daa5323.png)
![8ff8ccbd621010836fa5e84c64ff3e18.png](../_resources/8ff8ccbd621010836fa5e84c64ff3e18.png)
- 注意，不同的变量也有可能probability mass function 完全相同
![7b264dd508e27d7f7d2f13c78bc953f9.png](../_resources/7b264dd508e27d7f7d2f13c78bc953f9.png)
## 3.3
![b9788c82963f47d1b2ba3a33dcc3e9c7.png](../_resources/b9788c82963f47d1b2ba3a33dcc3e9c7.png)
![1a742971a86a28101f9e790aad18a109.png](../_resources/1a742971a86a28101f9e790aad18a109.png)
![9b6bd19dcbbf8a2f15c041f4664d9857.png](../_resources/9b6bd19dcbbf8a2f15c041f4664d9857.png)
![54a034ddf112d90138067df56c52b463.png](../_resources/54a034ddf112d90138067df56c52b463.png)
## 3.4
- 超几何分布
![5b9b5ef75d50368500dc52e15b6dce9b.png](../_resources/5b9b5ef75d50368500dc52e15b6dce9b.png)
## 3.5
- 离散均匀分布
![15f8a323078d1fafbd9e6bd6b8310985.png](../_resources/15f8a323078d1fafbd9e6bd6b8310985.png)
## 3.6
![6e5b49f24cad7621df14d41b5404b203.png](../_resources/6e5b49f24cad7621df14d41b5404b203.png)
![a4710ed2b0249bb480439521faac9416.png](../_resources/a4710ed2b0249bb480439521faac9416.png)
## 3.7
![72c75d11054b6bdc340748235899fb8d.png](../_resources/72c75d11054b6bdc340748235899fb8d.png)
- 对随机变量进行(从实数到实数的)函数变换得到的还是随机变量
- We can think of the distribution of a random variable as a map or blueprint describing the r.v. Just as different houses can share the same blueprint, different r.v.s can have the same distribution, even if the experiments they summarize, and the sample spaces they map from, are not the same.
## 3.8
![70cd5298ed7d5c55fe0ac782fbea84a5.png](../_resources/70cd5298ed7d5c55fe0ac782fbea84a5.png)
- 若两变量独立，任何它们的函数也是独立的
  r.v.s:random variable sequence
  
![74238a5ad30bab17c08f5f348618cc67.png](../_resources/74238a5ad30bab17c08f5f348618cc67.png)
![c9df4e1eb72c48f4d88264d9a17a1fef.png](../_resources/c9df4e1eb72c48f4d88264d9a17a1fef.png)
![f5fb5ed5ac8b030fc14a665cc26967f2.png](../_resources/f5fb5ed5ac8b030fc14a665cc26967f2.png)
## work
![3a6e94cdc437cb1f28ee781a8b0dff02.png](../_resources/3a6e94cdc437cb1f28ee781a8b0dff02.png)
![33337c05bab42777b8f4fcfb4f70484d.png](../_resources/33337c05bab42777b8f4fcfb4f70484d.png)
- 生日问题，人一个一个的来，所以要区分，是排列

## word
isomorphic:同构的
# unit4 contineous random variables
## 4.1 Probability density function
![0b43b0ee54e454dd6957ed35eb096faa.png](../_resources/0b43b0ee54e454dd6957ed35eb096faa.png)
- 对于连续型随机变量，可以任意的舍弃端点
## 4.2 Uniform
![e6fdf077ccb17058c8338a7c7f8035e4.png](../_resources/e6fdf077ccb17058c8338a7c7f8035e4.png)
![005b57bc1864f6548841a24a43467349.png](../_resources/005b57bc1864f6548841a24a43467349.png)
## 4.3 university of the uniform(均匀分布的普适性)
- 任何数据集的百分位分布一定是均匀的
- other name：probability integral transform, inverse transform sampling, the quantile transformation, and even the fundamental theorem of simulation.
![2bd1c048c61c7fb6b54f4301fc20818d.png](../_resources/2bd1c048c61c7fb6b54f4301fc20818d.png)
![23a91e35c0511f96db8319d544878b3b.png](../_resources/23a91e35c0511f96db8319d544878b3b.png)
- fact(U服从标准均匀分布)
```math
P(U\leq u)=u\  for\ u\in(0,1) 
```
## 4.4 normal
![b7808e8b6637d6568e14c335d713e5d9.png](../_resources/b7808e8b6637d6568e14c335d713e5d9.png)
![97bf0bb8f42f58d3c7f96e0773411f4d.png](../_resources/97bf0bb8f42f58d3c7f96e0773411f4d.png)
![f289cfbfb74bd471b78225fc7aea3c2c.png](../_resources/f289cfbfb74bd471b78225fc7aea3c2c.png)
![14dec13a5fc41db624fc1c83c3b1b889.png](../_resources/14dec13a5fc41db624fc1c83c3b1b889.png)
## 4.5 exponential
![69d9f6999caefd2ecf5865c5c7884fb0.png](../_resources/69d9f6999caefd2ecf5865c5c7884fb0.png)
![96385ae275c1754e02a47728c946aea1.png](../_resources/96385ae275c1754e02a47728c946aea1.png)
## 4.6 poisson processes
![0127988d23d7784fde247a9677408dad.png](../_resources/0127988d23d7784fde247a9677408dad.png)
- 在泊松过程中，t秒内无抵达的概率和t秒时抵达数为0是同一事件，所以有
```math
P(T_1>t)=p(N_t=0)=e^{-\lambda t}
```
![ea4077b68a7883e1843930e38be8d9cd.png](../_resources/ea4077b68a7883e1843930e38be8d9cd.png)
## work
![4fe413cb701b6985e88b57bc2648a2dd.png](../_resources/4fe413cb701b6985e88b57bc2648a2dd.png)
- 对称性的理解：两者是独立同分布，
```math
P(T_a>T_b)=P(T_b>T_a)
```
而两者包含了所有的情况，和为1
### 泊松过程：(“计数-时间对偶性” (Count-Time Duality))
#### 无记忆性：
时间角度，服从指数分布，等了多久对接下来还要等多久毫无影响
#### 计数角度：
```math
P(N(t)=k)=P(k\ cars\ arrive\ in\ t\ hours)=\frac{( (λt)^k * e^{-λt} )} { k!}
```
- 小于3，求和0,1,2
## word
analogous:类似的
quantile：分位数
# unit5 averages law of large numbers,and central limit theorem
## 5.1 expectation
![545c6548230b835c794dc873b0333e85.png](../_resources/545c6548230b835c794dc873b0333e85.png)
$E(X-3)^2=E((X-3)^2)$
## 5.2  Linearity of expectation
超几何的期望： $E(X)=\frac{nw}{w+b}$
## 5.3 Geometric and Negative Binomial
![9f67d5daa50736ef396d1de13ac800ee.png](../_resources/9f67d5daa50736ef396d1de13ac800ee.png)
- 这个是没考虑成功的那次的，考虑的叫first success distribution(FS)
![5fb8d0badf1e7fb9d7307a34d77d19fc.png](../_resources/5fb8d0badf1e7fb9d7307a34d77d19fc.png)
几何分布的期望计算
![6dd93f87e9d6398827dcded1ad14612c.png](../_resources/6dd93f87e9d6398827dcded1ad14612c.png)

![39e0301bfc27eb3c335270c37f986429.png](../_resources/39e0301bfc27eb3c335270c37f986429.png)
![ed38d595312266e2c5da02435ebf23cd.png](../_resources/ed38d595312266e2c5da02435ebf23cd.png)
- e.g
![0888cc5eaf9a1f8bfb0b914300c93ad7.png](../_resources/0888cc5eaf9a1f8bfb0b914300c93ad7.png)
![76d13ca39e42f0bdd6f4aa6afaa0212c.png](../_resources/76d13ca39e42f0bdd6f4aa6afaa0212c.png)
- 函数的期望≠期望的函数(尤其当函数非线性时)
## 5.4  Indicator random variables and the fundamental bridge
![394a0c10d904c7908fcb10676f643379.png](../_resources/394a0c10d904c7908fcb10676f643379.png)
![e81f8b705e2d7d36322786a10051c11f.png](../_resources/e81f8b705e2d7d36322786a10051c11f.png)
- 强大之处：无需是各变量独立的

![d5bbfaa0215c45368700d53b446b81e8.png](../_resources/d5bbfaa0215c45368700d53b446b81e8.png)
## 5.5 Law of the unconscious statistician (LOTUS)
![e11ea9b54c01868a8d656546011dc09d.png](../_resources/e11ea9b54c01868a8d656546011dc09d.png)
## 5.6 varience
![8dcae73e26b5df9d09ea7b0f6b347ff4.png](../_resources/8dcae73e26b5df9d09ea7b0f6b347ff4.png)
![2bbd9e4e9f6621415c2e372fd5b65dd5.png](../_resources/2bbd9e4e9f6621415c2e372fd5b65dd5.png)
## 5.7 poisson
![38c16a8207666193b472a4886566b23e.png](../_resources/38c16a8207666193b472a4886566b23e.png)
其均值和方差均为 
$\lambda$
![5e87fe8a152e588ba6fe512def5f2ce7.png](../_resources/5e87fe8a152e588ba6fe512def5f2ce7.png)
![e32c8377be6b99e0af07f66929b3e50f.png](../_resources/e32c8377be6b99e0af07f66929b3e50f.png)
## 5.8 Expectation of a continuous random variable
![62c47d235dcf29d370da5c44d0687ac3.png](../_resources/62c47d235dcf29d370da5c44d0687ac3.png)
![557d100b603fe83086711cb0550b4ffb.png](../_resources/557d100b603fe83086711cb0550b4ffb.png)
## 5.9 Law of Large Numbers
![0e06f555f20a93cbb051d945272988e3.png](../_resources/0e06f555f20a93cbb051d945272988e3.png)
## 5.10 Central Limit Theorem
![c52a52959cca4626c417504f0636f13f.png](../_resources/c52a52959cca4626c417504f0636f13f.png)
- CLT也表明一堆独立同分布的随机变量序列之和趋近于一个正态分布
![e45ec2963c4771afc6e6259307c38d53.png](../_resources/e45ec2963c4771afc6e6259307c38d53.png)
这个分布没有有限的均值和方差，所以大数定律和中心极限定理都用不了
## work
- 算同时属于两个人的朋友，算a的：从b的朋友选一部分再从剩下的选一部分
## word
asymptotic:渐进的
skewed：歪斜的，曲解的
# unit6 Joint Distributions and Conditional Expectation
## 6.1 Joint, marginal, and conditional distributions
![75368620244221c4d314e34b1494b82a.png](../_resources/75368620244221c4d314e34b1494b82a.png)
CDF的可视化很困难，PMF用的更多
![0fc2c9927eef93134c943fc638a33007.png](../_resources/0fc2c9927eef93134c943fc638a33007.png)
![03c8e59776d9d5c924f7c240ee031bfe.png](../_resources/03c8e59776d9d5c924f7c240ee031bfe.png)
![8f2affe3fc104894717644f7805af623.png](../_resources/8f2affe3fc104894717644f7805af623.png)
![ea74165fd02ec2a9c587d04882d20ea6.png](../_resources/ea74165fd02ec2a9c587d04882d20ea6.png)
### 鸡蛋例子
问题描述:鸡生蛋的数量(N)服从泊松分布($\lambda$)，每个蛋是否孵化服从二项分布
X为孵化成功的，Y为孵化失败的，其联合分布
```math
P(X=i,Y=j)=\frac{e^{-p\lambda}(p\lambda)^i*e^{-q\lambda}*(q\lambda)^j}{i!*j!}
```	

可以发现可视为X，Y均服从泊松分布，且相互独立
![77de1c4671aeb367154bc815d760968b.png](../_resources/77de1c4671aeb367154bc815d760968b.png)		

唯一由pdf得到非零的概率的方法就是沿着一个区域积分（沿着线积分也是0）
![fe68badbe918ced5ada7239d3a382db0.png](../_resources/fe68badbe918ced5ada7239d3a382db0.png)
![e2afb2c6ef10cd7749efab26d390ff52.png](../_resources/e2afb2c6ef10cd7749efab26d390ff52.png)
![f53a8682dc7bc3607dfa1507993ec893.png](../_resources/f53a8682dc7bc3607dfa1507993ec893.png)
- 四种(连续和离散组合)
![a5b5b33d942b0f58a96b9a098089dba1.png](../_resources/a5b5b33d942b0f58a96b9a098089dba1.png)
![3de50dd100d0cde451fecab6f3ed2e72.png](../_resources/3de50dd100d0cde451fecab6f3ed2e72.png)
![001361ab0e0b5efd0c652773b113beed.png](../_resources/001361ab0e0b5efd0c652773b113beed.png)
## 6.2 Covariance and correlation(协方差和相关性)
![10e723ee1cd3eed27bfdf0922b1d2088.png](../_resources/10e723ee1cd3eed27bfdf0922b1d2088.png)
- 若x，y是独立的(independent)则是无关的(uncorrelated),即协方差为0
- 独立=>无关，但是逆命题不成立
![901fd6c609a38acc8a3aed05cea97c68.png](../_resources/901fd6c609a38acc8a3aed05cea97c68.png)
![5c19c8f3af6ee870c86cea3efdc914c2.png](../_resources/5c19c8f3af6ee870c86cea3efdc914c2.png)
上一个定义会受到各变量的测量用的单位的影响，所以用下面这个排除量纲影响
![7d3e75c535a9ce4f40ed58319f4cd62a.png](../_resources/7d3e75c535a9ce4f40ed58319f4cd62a.png)
correlation总是位于-1到1之间
![50410afe7f77113234ef5ce5d7a6e608.png](../_resources/50410afe7f77113234ef5ce5d7a6e608.png)
## 6.3 Multinomial(多项)
![b83186f307f0355ac0211b2b0523b693.png](../_resources/b83186f307f0355ac0211b2b0523b693.png)
![ce41be99773acad6f74ef0b7bc42b5b2.png](../_resources/ce41be99773acad6f74ef0b7bc42b5b2.png)
![86e7223e5d1ad029f11cb40f8434ae5f.png](../_resources/86e7223e5d1ad029f11cb40f8434ae5f.png)
## 6.4 Multivariate Normal(MVN)
![13a8fcd0c92d1b0856505197b45ff17c.png](../_resources/13a8fcd0c92d1b0856505197b45ff17c.png)
MVN可以推各部分是正态的，反过来不行
![e8580b7e2a58526e9c773c4a89e72f86.png](../_resources/e8580b7e2a58526e9c773c4a89e72f86.png)
![c72ad69cb6e54f9e7b08be039d1a906a.png](../_resources/c72ad69cb6e54f9e7b08be039d1a906a.png)
- 指定一个多项正态分布
	- 均值向量（包含每个随机变量的均值）
	- 协方差矩阵(k*k)(其实还需要每个的方差，但是对角线那里已经指明)

![c46b0ee4ebd66406a964d12a89256fa8.png](../_resources/c46b0ee4ebd66406a964d12a89256fa8.png)
![ef7e0dd276bcdd251ca76a851d8cd4b8.png](../_resources/ef7e0dd276bcdd251ca76a851d8cd4b8.png)
## 6.5 Conditional expectation
![4bdf82b2b737d12c0477242e606e3921.png](../_resources/4bdf82b2b737d12c0477242e606e3921.png)
![5bd98eb87e9e3d82224937a03815328d.png](../_resources/5bd98eb87e9e3d82224937a03815328d.png)
- importance of condition on every situation
![cfaaa7b198cb0e3b62fb3ad63c6fa899.png](../_resources/cfaaa7b198cb0e3b62fb3ad63c6fa899.png)

![d10269de991c86e27c1f3090ff2a4011.png](../_resources/d10269de991c86e27c1f3090ff2a4011.png)
e.g:骰子
- 另一种解法：用FS
![2a2dc7ea14832dc5d3d4b3c900ef2f2a.png](../_resources/2a2dc7ea14832dc5d3d4b3c900ef2f2a.png)
![a4c948ea48bd104c80683dbc4530266d.png](../_resources/a4c948ea48bd104c80683dbc4530266d.png)
![2f6699e4bf4aa5d8c28762cac4bfda8f.png](../_resources/2f6699e4bf4aa5d8c28762cac4bfda8f.png)
intuition：看一步进步之后会不会再回去
## 6.6 Conditional expectation given a random variable
![3f4845924d027c4b221192e874d927be.png](../_resources/3f4845924d027c4b221192e874d927be.png)
## 6.7 Adam's law and other properties of conditional expectation
![04ced313af5535a9afb86f83b580990f.png](../_resources/04ced313af5535a9afb86f83b580990f.png)
proof for adam's law
![412ab2813fe26a495bc64a7e6adb2395.png](../_resources/412ab2813fe26a495bc64a7e6adb2395.png)
对等式两边的随机变量可以同时求期望和方差(协方差)
## 6.8 Eve's law and conditional variance
![cbd939de62c7fc50d5379462c2709555.png](../_resources/cbd939de62c7fc50d5379462c2709555.png)
![0ca25fde2f015dbe4f9bc37009a5902c.png](../_resources/0ca25fde2f015dbe4f9bc37009a5902c.png)
- between group variation:$Var(E(Y|X))$
- 
- within-group variation:$E(Var(Y|X))$
- 

![83dd28d07fa69a3dd63c21d95b97a702.png](../_resources/83dd28d07fa69a3dd63c21d95b97a702.png)
![9dd697d27744e2ca71d29d4ae769bb1e.png](../_resources/9dd697d27744e2ca71d29d4ae769bb1e.png)

## work
![07c79e6875fef2c29e8f10ae510d560b.png](../_resources/07c79e6875fef2c29e8f10ae510d560b.png)
- 三条腿的椅子不稳==所有腿在一个半圆以内

![f451239e957c0c117417b1ee05bb6ca6.png](../_resources/f451239e957c0c117417b1ee05bb6ca6.png)
![c781739f55d71bed7d4f095b995d89d1.png](../_resources/c781739f55d71bed7d4f095b995d89d1.png)
## word
reciprocal：互惠的
lump:块
unwieldy：笨重的
albeit:尽管
degenerate:退化
contour：轮廓
marginal:边缘

# 7. markov chain
## 7.1 Markov property and transition matrix
![03708d06cd7cefb179c38c54e031d65e.png](../_resources/03708d06cd7cefb179c38c54e031d65e.png)
![3c894dc48e760ac46392d34afec6826b.png](../_resources/3c894dc48e760ac46392d34afec6826b.png)
![8976fb63f2aba9dd6e972962ef4c5e56.png](../_resources/8976fb63f2aba9dd6e972962ef4c5e56.png)
```math
q^{(n)}_{ij}is\ the (i,j) entry\ of\ Q^n
```
![4dc672d38559170016d4c06e772e8793.png](../_resources/4dc672d38559170016d4c06e772e8793.png)
## 7.2 Classification of states
![50c23b09c84d22a2c720791b6c3e8a76.png](../_resources/50c23b09c84d22a2c720791b6c3e8a76.png)
- 若i是一个马尔科夫链的transient state,设从i出发而不会再回到i的概率为p，这个链条从i开始，永远离开之前回到i的次数服从Geom(p)

  
![5b1fa94801559509ee4de1b7946b2695.png](../_resources/5b1fa94801559509ee4de1b7946b2695.png)
- irreducible implies all states are recurrent(反过来不一定成立)
- 一个马尔科夫链内至少一个是recurrent的
- 周期的定义：
![a0898e98f73d991d074aba235c24b684.png](../_resources/a0898e98f73d991d074aba235c24b684.png)

$d(i)=gcd\{n\ge1:p^{n}(i,i)\gt0\}$
## 7.3 Stationary distribution(also known as:steady-state distribution)
![8e33a569fddb873a0c42e050fd3329aa.png](../_resources/8e33a569fddb873a0c42e050fd3329aa.png)
![aef0a4abfb6fb689bf55ac18cbea1fcc.png](../_resources/aef0a4abfb6fb689bf55ac18cbea1fcc.png)
![13daeb829bfca23b38284752bfc6c565.png](../_resources/13daeb829bfca23b38284752bfc6c565.png)
![fc85a0e07945208844437ab9551f1767.png](../_resources/fc85a0e07945208844437ab9551f1767.png)
### google pagerank
视各网站的链接形成的网络为马尔科夫链，看其收敛之后，修正如下(为了给网络一定的再生长能力)	
```math
G=\alpha Q+(1-\alpha)\frac{J}{M}
```

```math
tG^n->s \ as\ n->∞
```
其中M为矩阵的size，J为全一矩阵
## 7.4 Reversibility(可逆性)
![a6a5c95ce63a3d7d12bc5906810836d4.png](../_resources/a6a5c95ce63a3d7d12bc5906810836d4.png)
- reversible implies stationary

### three types of markov chain that's reversible
- first
![6c115ced8b5e7598b529bbacc181c67e.png](../_resources/6c115ced8b5e7598b529bbacc181c67e.png)
- second
  	- if the Markov chain is a random walk on an undirected network, then there is a simple formula for the stationary distribution.(可以证明就是成比例缩放其各点的度数向量(就是每个点连出去多少根))
- third
	- Third and finally, if in each time period a Markov chain can only move one step to the left, one step to the right, or stay in place, then it is called a birth-death chain. All birth-death chains are reversible.
	- ![7a5c56941b311161f3eaa55a0952ca29.png](../_resources/7a5c56941b311161f3eaa55a0952ca29.png)
	- 然后解方程使 $S_1$ 满足和为1即可
棋盘类：注意很好的对称性，一般按可达到的状态分成几个状态向量(每种的个数与度数的乘积计算)
![7db161a97efc9f32ad07259d9fea2dd4.png](../_resources/7db161a97efc9f32ad07259d9fea2dd4.png)
## word
transient:易变的，短暂的
irreducible：不可约
aperiodic:非周期性
greatest common divisor:最大公约数
diluted:经稀释的，稀的
teleport：传送