## MD Simulation

1. C原子类型不同需要有不同的力场模型参数，键长模型所需参数的数量是C原子类型的平方倍，键角模型为立方倍
2. 力场：**CHARMM**、**AMBER**、**OPLS**、**UFF**、**Drieding**
3. torsion = diheral（improper diheral）
4. MD描述的是接近平衡态的分子状态




#### gaussview 与Gaussian



1. 保存一个.gjf文件
2. 下载gaussian16.pbs（get命令，下载到shell的运行文件夹中）
3. 更改pbs文件第8行内容，改为gjf文件名
4. 再把gjf和pbs文件提交到自己的目录（使用sftp协议提交，put命令）
5. 然后SSH到自己的目录
6. 运行qsub 加自己的pbs文件，开始运行
7. 通过qstat命令或者打开任务log查看运行结果




task:

氧气形成双键和单键 那个更稳定



















