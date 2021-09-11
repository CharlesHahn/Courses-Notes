
# Protein Engineering

### 基础

#### 绪论

1. 蛋白质工程：以**蛋白质分子结构规律与其生物功能之间的联系**作为基础，通过化学、物理、分子生物学等手段进行基因修饰或者基因合成，改造现有的蛋白质或者创造新的蛋白质，以满足人类生产生活的需要。

2. 基因工程和蛋白质工程的比较：两者都改造基因，都属于分子水平；基因工程没有新的基因型产生，使用的是原来就有的蛋白；蛋白质工程有**新基因型**产生并创造**新的蛋白**；蛋白质工程是以基因工程作为基础，是基因工程的应用和延伸。

3. 酶工程与蛋白质工程：酶工程注重对于已存酶的合理充分利用和大量制备，蛋白质工程注重于对于现有酶的改造。

4. 蛋白质工程起源：82年winter通过基因定位诱变获得改性的络氨酸tRNA合成酶；**83年**Ulmer提出蛋白质工程。

5. 研究内容：通过蛋白质结构分析为基础，进行蛋白质的结构和功能的设计和预测，最终创造出新的蛋白质。

6. 支撑技术：蛋白质结构解析技术、生物信息学分析技术、定点突变等遗传操作技术。

#### 蛋白质结构基础

7. 氨基酸
   - 脂肪族：
     + 甘氨酸（glycine）（gly) G
     + 丙氨酸（alanine）（ala) A
     + 缬氨酸（valine）(val) V
     + 亮氨酸（leucine）(leu) L
     + 异亮氨酸（isoleucine）(ile) I
   - 苯环： 
     + 苯丙氨酸（phenylalanine）（phe) **F**
     + 络氨酸（tyrosine）（tyr) **Y**
     + 色氨酸（tryptophan）（trp) **W**
   - 碱性： 
     + 赖氨酸（lysine）（lys) **K**
     + 精氨酸（arginine）（arg) **R**
     + 组氨酸（histidine）（his) H
   - 羟基： 
     + 丝氨酸（serine）（ser) S
     + 苏氨酸（threonine）（thr) T
   - 酸性： 
     + 天冬氨酸（aspartate）（asp）**D**
     + 谷氨酸（glutamate）（glu) G
   - 酰胺： 
     + 天冬酰胺（asparagine）（asn）**N**
     + 谷酰胺（glutamine）（gln）**Q**
   - 含S ： 
     + 半胱氨酸（cysteine）（cys）C
     + 甲硫氨酸（methionine）（met）M
   - 特殊环： 
     + 脯氨酸（proline）（pro）p

8. 构型（configuration）：一个分子中原子的的特定空间排布
  - 构型转换需要有共价键的断裂和连接
  - 不同构型的分子除镜面操作之外不能以任何方式重合
  - **手性**是构型
  - 化学上可以分立，不能用单键旋转来相互转换

9. 构象（conformation）：组成分子的原子绕单间旋转所得到的不同的分子中原子的空间排布
  - 构象转换时不需要有共价键的断裂和连接
  - 化学上不可以分立，存在各种构象之间的动态平衡，存在优势构象
  - **旋转异构体rotamer**：以优势构象出现的氨基酸残基

10. α-helix：
  - 多肽链中的各个肽平面围绕同一轴旋转，形成螺旋结构
  - 螺旋与螺旋之间形成氢键，氢键的取向几乎与轴向平行，具有极性（N+、C-）（结构：C-O...H-N)
  - 螺距0.54nm，3.6个氨基酸残基 
  - 两亲性（amphipathicity）：**螺旋一侧分布亲水残基，另一侧分布疏水残基**，对生物火星有着重要作用

11. β-sheet：
   - 氢键在片层间形成而不是片层内
   - 折叠片上的侧链都垂直于折叠片的平面，并且交替地从平面上下两侧伸出

12. 环肽链（loop）：
   - 回折reverse turn：
       + β-turn：四个氨基酸构成，第一个氨基酸残基的-C=O与第四个残基的-N-H形成氢键，此环状结构不稳定
       + γ-turn：三个氨基酸残基构成的转折
   - β-hairpin：
       + β-hairpin
       + random coil

13. 蛋白质空间结构层次：
   - primary structure：多肽链中氨基酸的排列顺序，二硫键的数目和排列方式
   - secondary structure：多肽链主链骨架中的若干肽段，各自沿着某个轴盘旋或者折叠，并以氢键维系，从而形成的有规则的构象，不涉及氨基酸残基构象
   - motif：介于蛋白质二级结构和三级结构之间的空间结构，只相邻的二级结构单元组合在一起，排列成有规则的在空间结构上能够辨认的二级结构组合体，并充当三级结构的构件（block building），如αα、βββ
   - domain：在二级（超二级）结构上形成的三级结构局部折叠域，在三维空间中可以明显区分和相对独立，有一定的生物学功能，通常由两三个结构单位组成，一般是α螺旋、β折叠、环
   - tertiary structure / submit：
     + 多肽链在各种二级结构的基础上再进一步卷曲折叠形成的具有一定规律的三维空间结构
     + 由二级结构元件、超二级结构和结构域构成
     + 包括相聚较远的肽段之间的几何相互关系和侧链在三维空间中的相互关系
     + 三级结构由三计算的长程顺序决定，维系力有氢键、疏水键、离子键和范德华力等
   - quaternary structure：
       + 具有两条或以上的独立三级结构的多肽链组成的蛋白质，多肽链键通过次级键相互组合形成的空间结构
       + 每个具有独立三级结构的多肽链单位成为亚基
       + 亚基之间不含共价键，次级键的结合也比二三级结构疏松

14. 维系蛋白质结构的力：
   - 肽键
       + 氨基酸的连接
   - 二硫键
       + 和肽键一起维持蛋白质的一级结构
   - 氢键
       + 维持蛋白质二级结构的主要作用力
   - 离子键
   - 疏水作用
   - 范德华力

15. 变性复性：因为物理或者化学的因素使得蛋白质分子的**空间构象发生改变或者被破坏**，导致其**生物活性丧失**和一些**理化性质的改变**；复兴后构象复原，活性恢复。
   变性的本质：蛋白质空间结构改变或者破坏（次级键的破坏），不涉及蛋白质一级结构的改变或者肽键的断裂

16. 化学修饰的目的：研究蛋白质结构和功能关系的重要手段，也是一种设计蛋白质的重要手段。
   侧链的化学修饰：
   - 氨基的修饰
   - 羧基的修饰
   - 巯基的修饰
   - 二硫键的修饰
   - 酰化及其相关反应
   - 烷基化反应
   - 氧化还原反应
   - 芳香环取代反应
   - PEG化（聚乙二醇化）

17. 蛋白质的分子生物学改造
   - 基因突变（gene mutagenesis）：指在**基因水平上**对编码的蛋白质进行改造，并在表达后用来研究蛋白质**结构和功能**的一种方法
     + 定点突变：（site directed mutagenesis）在体外对已知DNA序列进行替换、增删特定位点的核苷酸，改变蛋白质结构中的氨基酸残基，从而获得所需功能的突变蛋白质。
     + 定向进化：（directed protein evolution）不需要事先知道蛋白质结构和功能的关系，通过实验反复改造遗传多样性，结合文库进行高通量筛选，进而获得理想性状或者全新功能蛋白质的一种人工进化策略。

18. 蛋白质的热力学第二定律：
   - 熵判据：系统的各种过程都是向着熵增大的方向进行。
   - 自由能判据：ΔG = ΔH - T ΔS

19. 蛋白质折叠的热力学定律
   - 熵判据和蛋白质折叠
     + 未折叠的状态包含很多具有不同构象的分子
     + **疏水作用**是多肽链折叠的主要驱动力，疏水作用的主要动力来源来自于蛋白质溶液体系的**熵值**的增加。
   - 吉布斯自由能判据
     + **ΔG总 = ΔH链+ΔH溶剂‐TΔS链‐TΔS溶剂**
     + 折叠态比伸展态更加高度有序化，因而ΔS是负数，则‐TΔS链为正值
     + 折叠态蛋白质中疏水侧链主要是通过范德华力彼此相 互作用,而伸展态蛋白质的疏水侧链和溶剂分子间存在 相互作用,其作用力比范德华力强。结果导致ΔH链对疏 水侧链为正值,从而有利于伸展态
     + ΔH溶剂对疏水侧链是负值,有利于折叠态。这是因为蛋白质处于折叠态时,许多水分子之间的相互作用将代替水分子和疏水侧链的相互作用 
     + **ΔH链与ΔH溶剂值都不大,一般对折叠不起主要作用**
     + 蛋白质折叠过程中会打破水的有序化,则ΔS溶剂为较大的正值,因而 有利于折叠态
     + 对于典型的蛋白质来说,对折叠结构的稳定性做出单项大贡献的 是疏水残基引起的ΔS溶剂
     + **蛋白质折叠结构是生理条件下自由能低的构象**。因此,从吉布斯自由能的变化值来考虑,多肽链的折叠是热力学中的自 发过程

20. 蛋白质的稳定性：指**净作用力的净余额**，其决定着蛋白是处于天然构象还是变性状态；稳定性主要是指物理热力学上的稳定性，不是化学稳定性。

21. 影响蛋白质稳定性的因素：
   - pH：蛋白质在等电点附近稳定性较强
   - 配基结合：结合配基（酶、抑制因子）之后稳定性较强，蛋白质的活性中心与金属离子结合
   - 二硫键：
     + 胞外蛋白含有二硫键，胞内蛋白一般没有二硫键
     + 蛋白质二硫键断裂或者还原后再被氧化会导致蛋白质变性
     + 二硫键可以通过交联而降低非折叠态的构象熵来增强天然态的稳定性（降低了非折叠态的自由能）
   - 氨基酸残基对于蛋白质稳定性的贡献不是一样的；天然态下位于蛋白质内部的残基要比外部和溶剂接触的残基对于稳定性的贡献要大

#### 蛋白质折叠 

22. 新生肽链的折叠：新生肽链在空间中的盘曲折叠以及化学修饰、跨膜转运、亚基组装、水解激活等的一整个**肽链的成熟过程**
23. protein folding：从体内新生的多肽链或者体外变性的多肽链的一维线性氨基酸序列转变成具有三维结构的活性氨基酸的过程。
24. Anfinsen：
   - 理论：多肽链的氨基酸序列包含了形成热力学上稳定的天然构象所需的全部信息
   - 一级结构决定高级结构
   - Anfinsen贡献：
     + 氨基酸一级结构决定高级结构 —— 蛋白质折叠的热力学定律
     + 第一个发现二硫键异构酶
     + 亲和层析蛋白
     + 合成葡萄杆菌核酸酶 —— 固相合成
25. 体外蛋白质折叠和体内新生肽链折叠的不同：
   - 完整肽链在试管内的重折叠相当于翻译后折叠，新生肽链是一边合成一边折叠
   - 细胞内新生肽链的折叠是一个比体外蛋白质折叠快得多的过程
   - 温度、浓度、pH不同
   - 细胞内存在“大分子拥挤”现象
26. 细胞内的蛋白质折叠是在较高的温度、较高的蛋白浓度和较为拥挤的环境中以**极高的速度和极高的保真度**进行的，存在着帮助蛋白。
27. 帮助蛋白：
    1. 分子伴侣（molecular chaperone）
    2. 折叠酶（催化与折叠直接有关的化学反应的酶）
       - 蛋白质二硫键异构酶（protein disulfide isomerase，PDI）
       - 肽基脯氨酰顺反异构酶（peptidyl prolyl cis-trans isomerase，PPI）
28. 分子伴侣：一大类相互之间没有关系的蛋白质，都可以帮助其他含有蛋白质的结构体在体内进行非共价的组装和卸装，但是并不是这些结构体在发挥生物学功能时的必要组成部分。
    1. 与酶的异同点：
       1. 分子伴侣的定义是功能上的
       2. 都参用促进一个反应但是并不褚希纳兹啊最终产物中
       3. **分子伴侣不具有高度专一性，催化效率很低，只是阻止错误折叠而不指导正确的折叠**
    2. 分子伴侣的作用：
       1. 识别折叠过程中的非天然结构，并与之结合，防止过早或者错误的相互作用进而阻止不正确的折叠，一致不可逆的聚合物的产生
       2. 首先识别折叠过程中折叠中间物的非天然构象，不理会天然构象
       3. 分子伴侣与早期形成的中间物相互作用而防止聚合，一旦聚合分子伴侣也没有作用
29. 第二遗传密码：无结构的氨基酸序列与具有完整生物学功能的蛋白质三维结构之间的关系
    1. 简并性：氨基酸序列不同的氨基酸可以具有相似甚至相同的结构
    2. 多义性：相同的氨基酸序列可以在不同的条件下折叠成不同的三维结构
    3. 全局性和复杂性：在序列上相距很远的氨基酸残基可以在空间上相距很近并彼此相互作用而影响蛋白质空间结构；后形成的肽链的构象可以对整体蛋白质结构进行影响
30. 蛋白质的质量控制：
    1. 翻译后质量控制：新生肽链在折叠和成熟的过程中因为各种各样的原因可能会发生错误，生物体内具有引导新生态链正确折叠和处理这些错误折叠的蛋白质的能力，防止非正常物质累积对细胞造成损伤。
    2. 翻译后质量控制方式：
       1. 由分子伴侣和靠消耗ATP的蛋白质水解酶组成
       2. 分子伴侣帮助正确折叠，蛋白质水解酶把不能继续正确折叠和错误折叠的蛋白质水解
31. 与折叠有关的构象病：
    1. 分子病：蛋白质中一个氨基酸残基变化导致的**地中海镰刀状红血球贫血症**
    2. 折叠病：蛋白质序列OK但是结构或者构象改变引起的疾病，或者由于错误折叠导致蛋白质分子聚集或不能正确转运到位
       1. 老年性痴呆症（Alzheimer syndrome）
       2. 帕金森（Parkinson disease）
       3. 某些肿瘤（抑癌基因突变导致其编码的蛋白质稳定性改变）
32. 分子图形表示方式：用不同的形式表示不同层次的结构
    1. 骨架式：用一定长度的线条连接相邻两个原子
       - 优点：易于移动、旋转、缩放
       - 缺点：立体感不强
    2. 棍球式：用实心小球代表原子，球与球之间用一定宽度的直线连接
       - 优点：直观、立体感强
    3. 填充式：以一定半径的实心球表示原子，半径取范德华半径
       - 优点：较强的立体感、
       - 缺点：图形操作时需要大量的消隐计算，速度较慢
33. 基于天然蛋白质结构的分子设计：
    1. 小改：定点突变或者化学修饰
    2. 中改：结构域进行拼接组装
    3. 大改：蛋白质完全从头设计
34. 蛋白质设计的目标及解决方法：
    1. 热稳定性：
       1. 引入二硫桥
       2. 增加内氢键数目
       3. 改善内疏水堆积
       4. 增加表面盐桥
    2. 对氧化的稳定性
       1. 把Cys转换为Ala或者Ser
       2. 把Met转换为Gln、Val、Ile或者Leu
       3. 把Trp转换为Phe或者Tyr
    3. 对重金属的稳定性：
       1. 把Cys转换为Ala或者Ser
       2. 把Met转换为Gln、Val、Ile或者Leu
       3. 代替表面羧基
    4. pH稳定性：
       1. 替换表面电荷集团
       2. His、Cys以及Tyr的置换
       3. 内离子对的置换
    5. 提高酶学性质
       1. 专一性的改变
       2. 增加逆转数（turnover number）
       3. 改变酸碱度
35. 甘氨酸、脯氨酸、丙氨酸：
    1. 分子量都比较小
    2. 灵活性：Gly > Ala > pro
    3. 甘氨酸基于有高度柔韧性、可在α-helix、β-sheet折叠处出现，常见于铰链区或者β-turnover，Gly在定点突变时一般不宜改变
    4. Pro比较刚性，常出现在β转角
    5. Ala常用作取代别的氨基酸的首选
36. 含硫氨基酸 —— 半胱氨酸、甲硫氨酸
    1. Cys、Met疏水值较高，常出现在分子内的疏水区
    2. Met具有较长的侧链，常出现在α螺旋中
    3. cys的还原性巯基可以形成二硫键，稳定蛋白质结构
    4. cys的还原性巯基可以以怕配位方式与金属结合
    5. 蛋白质设计中增加二硫键可以增加蛋白质的稳定性
37. 极性氨基酸 ——  丝氨酸、苏氨酸、络氨酸、组氨酸
    1. Ser、Thr、Tyr各含一个羟基，His侧链含有一个NH，所以都可以形成氢键，常出现在酶与第五结合的活性中心或者受体与配体结合的活性部位
    2. Ser蛋白酶、Thr激酶、Tyr激酶
    3. 血球蛋白、细胞色素b、锌指蛋白的活性部位都含有His
38. 带电氨基酸 ——  天冬氨酸、谷氨酸、赖氨酸、精氨酸
    1. Asp、Glu带负电，Lys、Arg带正电
    2. 带电性使得这些氨基酸常出现在分子表面，与水分子或者其他分子形成氢键
    3. Arg有时也在分子内部以盐桥的形式出现
    4. Asp、Glu与钙离子结合后，Lys、Arg也常出现在活性部位
39. 酰胺类氨基酸 —— 天冬酰胺、谷氨酰胺
    1. Asn、Gln虽然都是酰胺类氨基酸，但是Gln多了一个甲基，所以构象特征不同
    2. Gln常出现在α-helix螺旋的中间部分，Asn常出现在α-helix的起始段，改变主链走向
    3. Asn常与Ser和Thr一起，以Asn-X-Ser或者Asn-X-Thr的形式形成糖基化位点
40. 疏水氨基酸 —— 缬氨酸、亮氨酸、异亮氨酸、苯丙氨酸、色氨酸
    1. 侧链具有很强的疏水性，常在分子内部的疏水区，与二硫键和甲硫氨酸的疏水侧链紧密堆积，起稳定空间构象的空间
41. 氨基酸性质与蛋白质结构功能总结：
    1. AA多样性 —— 蛋白质多样性 —— 生物多样性
    2. 同属一组的，Val、Leu、Ile可以互相替换，Gly和Pro结构不同，Asn和Gln结构也不同，甭能替换
    3. 每个氨基酸与周围的氨基酸一起共同构成整个蛋白质的空间构象，孤立强调某一个氨基酸的作用力是不恰当的
    4. 分子设计时，纪要考虑各个氨基酸的构象，又要从结构层次上考虑整体的效应
42. Janus设计：
    1. β-sheet到α-helix
    2. 短程和长程作用力综合考虑
    3. 保留形成α-helix的残基而替换倾向于形成β-sheet的残基
    4. 引入与目标蛋白类似的盐键和电荷分布方式
    5. 引入Tyr来与目标蛋白相同并有利于折叠的检测
43. 与蛋白质分离纯化有关的理化性质：
    1. 溶解特性 ——  盐析、有机溶剂沉淀、等电点沉淀
    2. 分子大小 —— 透析、超滤、凝胶过滤、离心
    3. 带电特性 —— 电泳、离子交换层析
    4. 吸附特性 —— 吸附色谱
    5. 与配体特异性结合 —— 镍柱亲和层析
    6. 分子形状 ——  蛋白质结晶，梯度离心和电泳
    7. 变性和复性 ——  尿素变性析出然后复性
44. 蛋白质纯化的总原则：以合理的效率、速度、收率、纯度，将目标蛋白从细胞的全部其他成分特别是不想要的杂蛋白中分离出来，同时仍旧保留其生物学活性和化学完整性。
45. 蛋白质纯化的步骤：
    1. 选择实验材料、实验材料预处理
    2. 蛋白质的提取
    3. 蛋白质的粗分级
    4. 蛋白质的细分级
    5. 蛋白质的鉴定
46. 蛋白质的粗分级
    1. 使用蛋白质提取缓冲液提取实验材料之后，蛋白质提取液中蛋白质浓度往往较低，采用简单的方法进行蛋白质的浓缩，同时去除大量的杂质
    2. 硫酸铵分级沉淀、有机溶剂分级沉淀、超速离心、等电点沉淀、透析、超过滤、蛋白质结晶
47. 蛋白质的细分级
    1. 根据蛋白质分子大小、分子形状、分子表面特征或者分子带电情况进一步纯化
    2. 常用技术：层析和电泳
       - 分子筛层析
       - 离子交换层析
       - 疏水作用层析
       - 亲和层析
       - 羟基磷灰石层析
       - 电泳：带电颗粒在电场作用下，向着与其电性相反的电极移动
48. western blot：在电场的作用下将电泳分立的多态从凝胶转移到一种固相支持体，然后用这种多肽的特异抗体来检测
    1. 直接法：
       - 快速、没有二抗交叉反应引起的非特异性条带
       - 免疫反应性降低、无二级信号放大
       - 抗体标记时昂贵，使用不方便
    2. 间接法
       - 免疫特异性不受标记影响、信号放大灵敏度高（多个二抗结合位点）多种标记的二抗可供选择可选择不同的marker
       - 交叉反应引起的非特异性条带、额外的二抗孵育以及条件优化
    3. 间接法的操作流程：
       1. 电泳分离，转膜，固定蛋白到膜上
       2. 漂洗和封闭
       3. 一抗和蛋白质结合（小鼠单抗或者兔多抗）
       4. HRP，AP标记二抗与一抗-蛋白质复合物结合
       5. SuperSignal底物与二抗HRP，AP反应，显色或者发光
49. 晶胞（unit cell）：空间点阵的单位（大小和形状完全相同的六面体），晶体结构的最小单位
50. X射线的获得：
    1. 波长范围：10 ~ 0.1A
    2. 晶体的晶格常数处于X射线的波长范围内
    3. 衍射波的**衍射方向**（衍射波在空间的分布）和**衍射强度**和原子内原子的分布规律（**晶体结构**）有关
51. X射线衍射：
    1. 衍射方向取决于：晶体构型的几何性质（晶胞类型、晶面间距、晶胞参数等）
    2. 衍射的强度取决于：晶体的实质内容（原子种类、原子数量以及具体的分布排列）
52. 晶体（Crystal）：离子、原子或分子这些微粒在三维空间中**周期性重复排列**形成的、能够给出明锐衍射的固体结构
53. X射线衍射晶体结构测定优点：
    1. 分辨率高
    2. 不伤害样品
    3. 没有污染
    4. 相对快捷
    5. 能够得到晶体完整性的大量信息
54. X射线衍射晶体的缺点：
    1. 晶体构象是静态的，不能测定不稳定的过渡态的构象
    2. 很多蛋白质难以结晶，或者很难得到用于结构分析的足够大的晶体（**难以得到合适的结晶**）
    3. X射线衍射的工作流程较长
55. 核磁共振（nuclear magnetic resonance）：核磁矩不为零的核，在外磁场的作用下，核自旋能量级发生塞曼分裂，共振吸收某一特定频率的射频辐射（外加辐射的频率与原子核自旋进动的频率相同）
56. 化学位移：
    1. 在有机化合物中，各种氢核周围的**电子云密度不同**（结构中位置不同），导致共振频率有差异，即引起共振吸收峰的位移。
    2. 来源于核外电子云对于质子的磁屏蔽效应，大小和外加磁场强度成正比
57. 弛豫时间（relaxation times）
    1. 原子核从激发状态恢复到平衡排列状态的过程叫做弛豫过程，这段时间叫做弛豫时间
    2. 自旋晶格弛豫：（纵向弛豫t1），处于高能级的氢核将能量传递给周围的分子变成热运动而回到低能级状态
    3. 自旋-自旋弛豫：（横向弛豫t2），两个进动频率相同但是取向不同的磁性核在一定距离内互相交换能量，改变进动方向
58. NOE（nuclear overhauser effect 信号强度）：
    1. 当分子内有2个空间距离小于0.5nm的原子核时，如果 用双共振法照射其中一个核，使干扰场的强度增加到 刚好使被干扰的谱线达到饱和，则另一个靠近的原子 核的共振信号就会增加，这种现象称核欧沃豪斯效应 （NOE）
    2. 该效应的大小与原子之间距离的6次方成反比
59. 耦合常数(coupling constants）
60. 谱峰面积
    1. 峰面积与同类质子数成正比，仅能确定各类质子的相对比例
    2. 峰面积可以作为定量分析的基础
61. 谱图中化合物的结构信息：
    1. 峰的位移：各类质子所处的化学环境（结构位置）
    2. 峰的裂分数：相邻碳原子上质子数（2 * 1/2 * n +1），n为相邻的质子数
    3. 耦合常数：确定化合物的构型
    4. 峰的数目：标志分子中磁不等性质子的种类
    5. 峰面积：各类质子的相对数目
    6. **不足**：即能确定质子（氢谱）
62. 核磁共振优点:
    1. 高分辨率
    2. 可以在溶液中操作，接近生理状态
    3. 分析并模拟出蛋白质的空间结构、与辅基和底物结合的情况以及酶催化的动态机理
63. 核磁共振不足：
    1. 样品分子量要足够小（< 50KD）
    2. 对于不溶的蛋白质比较困难（膜蛋白）
    3. 实验周期长（ > 1年）
64. 电子显微技术：
    1. 直接获得分子的形貌信息
    2. 适合解析那些不适合用X射线和NMR技术分析的样品
    3. 适合捕捉动态结构变化信息
    4. 同其他技术结合可以获得分子复合体的高分辨率的结构信息
    5. 电镜图像中包含了相位信息，所以相位确定上要比X射线晶体学直接和方便
    6. **缺点**：分辨率低，小分子蛋白效果不佳
65. CD（Circular Dichroism）：用于蛋白质折叠、构象研究、酶动力学等
66. Fluorescence Resonance Energy Transfer (FRET)：当一个荧光分子（又称为供体分子）的荧光光谱与另一个荧光分子（又称 为受体分子）的激发光谱相重叠时，供体荧光分子的激发能诱发受体分 子发出荧光，同时供体荧光分子自身的荧光强度衰减
67. 生物芯片（biochip）：将大量分子探针固定于固相支撑物上后与带荧光标记的DNA或者样品分子进行杂交，通过检测每个杂交分子的杂交信号强度进而获得样品分子的数量和序列等信息
68. **生物芯片标准**：
    1. 有规则
    2. 显微尺度
    3. 平面的
    4. 特异性吸附
69. 生物芯片的制作方法：
    1. 接触点样法
    2. 原位合成法：寡聚核苷酸原位光刻DNA合成技术
    3. 喷墨法
70. 人类基因组学现存问题：
    1. 大量的新基因数据，缺乏蛋白质功能注释
    2. mRNA丰度与蛋白质丰度相关性不好
    3. 蛋白质合成之后还要经历后期的修饰
    4. 包含了多种蛋白质的细胞是如何运作的
71. 蛋白质组（proteome）：一个基因组、一种生物或者一种组织或细胞所表达的**全套**蛋白质
72. 蛋白质组学（proteomics）：研究细胞、组织或者生物体**蛋白质组成及其变化规律**的科学，是研究基因组DNA序列和基因功能之间的桥梁
73. 研究proteomics的原因：
    - 人类基因组学存在问题
    - 生物技术的发展
    - 计算机科学和生物信息学的发展
74. 蛋白质组研究整体技术的特点：
    - 规模化
    - 通量化
    - 自动化
75. 蛋白质组学技术目标：
    - 有效分离
    - 准确鉴定
    - 合理分析
76. 蛋白质组学研究手段：
    1. 蛋白质组研究核心 —— 用于分离的双向电泳（2-DE）
    2. 蛋白质组技术支柱 —— 鉴定技术
    3. 蛋白质组研究百科全书 —— 数据库
77. 差异蛋白组学：定量和定性的比较不同条件下的蛋白组，用以研究生化过程和发现biomarkers
78. 2DE(2 dimensional gel **electrophoresis**）：
    1. 第一向：**等电点聚焦分离**
    2. 第二向：SDS-PAGE
    3. 分辨率远高于任何其他一种单一的电泳方法，是目前最好的分析混合蛋白质样品的手段



### 英文

1. prion —— 阮毒体
2. amino —— 氨基酸
3. peptide unit —— 肽单位
4. configuration —— 构型
5. conformation —— 构象
6. rotamer —— 旋转异构体
7. stagged conformation —— 交错构象
8. loop —— 环肽链
9. turn —— 转角
10. **amphipathicity** —— 两亲性
11. helical wheel —— 螺旋转轮
12. reverse turn —— 回折（β转角或γ转角）
13. primary structure —— 一级结构
14. secondary structure —— 二级结构
15. motif —— 模体
16. domain —— 结构域
17. **tertiary** structure —— 三级结构
18. **quaternary** structure —— 四级结构
19. homology —— 同源
20. random coil —— 无规卷曲
21. block building —— 构件
22. hydrogen bond —— 氢键
23. **PEGylation** —— 聚乙二醇化
24. gene mutagenesis  —— 基因突变技术
25. site directed mutagenesis —— 定点突变SDM
26. diredted protein evolution —— 定向进化
27. protein folding —— 蛋白质的折叠
28. molecular chaperone ——  分子伴侣
29. triage —— 分诊治疗机制
30. Alzheimer syndrome  —— 阿尔兹海默症
31. Parkinson disease —— 帕金森综合症
32. **chromatography** —— 层析
33. **electrophoresis** —— 电泳
34. gel filtration —— 凝胶过滤
35. ion exchange —— 离子交换层析
36. hydrophobic interaction —— 疏水作用层析
37. affinity —— 亲和层析
38. unit cell  —— 晶胞
39. **crystal** —— 晶体
40. nuclear magnetic resonance —— NMR核磁
41. relaxation times —— 弛豫时间
42. coupling constants  —— 耦合常数
43. cicular dichroism —— 圆二色谱
44. biochip —— 生物芯片
45. proteome —— 蛋白质组
46. proteomics —— 蛋白质组学
































