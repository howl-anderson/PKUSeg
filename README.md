# LancoSeg��һ������׿Խ�����ķִʹ��߰�
LancoSeg�ں������µ����ѧϰģ�ͺʹ�ͳ��crfģ�ͣ����ܸ�Ч��֧�ֶ�����ִʡ�
## Ŀ¼
* [��Ŀ����](#��Ŀ����)
* [ʹ�÷�ʽ](#ʹ�÷�ʽ)
* [����ִʹ��߰������ܶԱ�](#����ִʹ��߰������ܶԱ�)
* [�������](#�������)
* [����](#����)

## ��Ŀ����

LancoSeg�ɱ�����ѧ����������-���Լ��������ѧϰ�о��������Ƴ���һ��ȫ�µ����ķִʹ��߰���LancoSeg�������¼����ص㣺

1. ϸ����ִʡ�����ѵ���˶��ֲ�ͬ����ķִ�ģ�͡����ݴ��ִʵ������ص㣬�û��������ɵ�ѡ��ͬ��ģ�͡�
2. ׼ȷ�ʸߡ�����ڴ�ͳ�Ĵ����ȵĵ�һģ�͵ļܹ������ǵ�ģ���ڲ�ͬ����������϶����и��õ����ܱ��֡�
3. ֧���û���ѵ��ģ�͡�������ģ�͵Ļ����ϣ�ģ�Ϳ��Ը����û��ṩ��ȫ�±�ע�����ݽ���ѵ����
4. �ṩ��fast��heavy���ִַ�ģʽ��fastģʽ�ڱ����о������ķִ�Ч����ͬʱ�����нϿ�ķִ��ٶȣ��ʺϴ��ģ������ʹ�á�heavyģʽ�ִ�Ч��һ��Ϻã������нϺ�ʱ���ʺ϶Էִ�Ч��Ҫ��ϸߵ��û�ʹ�á�

## ʹ�÷�ʽ
    * ����seg/bin/x64/ReleaseĿ¼�µ�seg.exe����windows�û���ֱ����cmd�����£�linux�����û���Ҫ����mono���
	* �ִ�ģʽ��[mono] LSTM.exe test [-mode] [-input file] [-output file]
    * ѵ��ģʽ��[mono] LSTM.exe train [-mode] [-train file] [-test file]
    * ���ı��ļ����������ע���ΪUTF8�ı���
### ����˵��
    test  �ִ�
    train ѵ��
    [-mode] ��ѡ������Ϊfast��heavy����ģʽ�� fastģʽ��crfģ��ʵ�֣�֧�ֿ��ٷִʡ�heavyģʽ�����ѧϰģ��ʵ�֣�֧�ָ߾��ȷִʡ�
    [-input] �û�ָ���Ĵ��ִ��ļ�
    [-output] �û�ָ���ķִʽ������ļ�
    [-trainFile] & [-testFile] �û���ע��ѵ�����ϣ�����֮���Ի��з��ָ�������֮���Կո�ָ�
    
### ��������
	mono LSTM.exe test fast data/input.txt data/output.txt 			linux�����£���fastģ�ͽ��зִ�
    LSTM.exe test heavy data/input.txt data/output.txt           windows �����£���heavyģ�ͽ��зִ�
	mono LSTM.exe train fast data/train.txt data/test.txt 		   ����ָ����ѵ���ļ��Զ���ѵ����ѵ��ģ�ͻᱣ�浽seg/bin/x64/Release/modelĿ¼��
	
### Ԥѵ��ģ��
    �ִ�ģʽ�£��û���Ҫ��seg/bin/x64/Release/model����Ԥѵ���õ����ݣ����ݿ�����https://drive.google.com/drive/folders/1X7Yfmfiakgt7DYE86IEFT1wZdrEhOasy ��ַ���أ����ݾ�����Ҫ���û������Զ����ѡ��ͬ��Ԥѵ��ģ�ͣ������ǶԲ�ͬģ�͵�˵����
    msra_fast��fastģʽ�£���MSRA���������ϣ���ѵ����ģ��
    msra_heavy��heavyģʽ�£���MSRA���������ϣ���ѵ����ģ��
    ctb_fast�� fastģʽ�£���CTB8�������ı��������ı��Ļ�������ϣ���ѵ����ģ��
    ctb_heavy��heavyģʽ�£���CTB8�������ı��������ı��Ļ�������ϣ���ѵ����ģ��
    weibo_fast��fastģʽ�£���΢���������ı����ϣ���ѵ����ģ��
    weibo_heavy��heavyģʽ�£���΢���������ı����ϣ���ѵ����ģ��
    
��ʹ��fastģʽ����������fastΪ��׺��β��ģ�ͣ���ʹ��heavyģʽ����������heavyΪ��׺��ģ�͡�MSRA�����ɵڶ�����ʺ���ִ���������ṩ��http://sighan.cs.uchicago.edu/bakeoff2005/ ����CTB8��LDC�ṩ��https://catalog.ldc.upenn.edu/ldc2013t21   ����weibo������NLPCC�ִʱ����ṩ��http://tcci.ccf.org.cn/conference/2016/pages/page05_CFPTasks.html ����


## ����ִʹ��߰������ܶԱ�
����ѡ��THULAC����ͷִʵȹ��ڴ���ִ������LancoSeg�����ܱȽϡ�����ѡ��Windows��Ϊ���Ի���������������(MSRA)�ͻ�����ı�(CTB8)�����϶Բ�ͬ����������ٶȺ�׼ȷ�ʲ��ԡ�����ʹ���˵ڶ�����ʺ���ִ���������ṩ�ķִ����۽ű������������£�

MSRA

|Algorithm | Time | F-score|
|:------------|-------:|------------:|
| jieba | 0.82s |81.45 |
| THULAC | 7.12s | 85.48 |
| LancoSeg-fast | 16.12s | 96.75 |
| LancoSeg-heavy | 83.01s | 96.86 |

CTB8

|Algorithm | Time | F-score
|:------------|-------:|------------:|
|jieba|1.29s|79.58
|THULAC|5.15s|87.77
|LancoSeg-fast|10.69s|95.64
|LancoSeg-heavy|48.33s|96.68

## ��ԴЭ��
1. LancoSeg����������ѧ���о�������ҵ�Լ����������о�Ŀ����ѿ���Դ���롣
2. ���л���������⽫LancoSeg������ҵĿ�ģ��뷢�ʼ���xusun@pku.edu.cnǢ̸�������Э�顣
3. ��ӭ�Ըù��߰�����κα�������ͽ��顣�뷢�ʼ���jingjingxu@pku.edu.cn��

## �������
* Jingjing Xu, Xu Sun. Dependency-based Gated Recursive Neural Network for Chinese Word Segmentation. ACL 2016: 567-572
* Xu Sun, Houfeng Wang, Wenjie Li. Fast Online Training with Frequency-Adaptive Learning Rates for Chinese Word Segmentation and New Word Detection. ACL. 253�C262. 2012 

   
## ����

Xu Sun �����򣬵�ʦ��,  Jingjing Xu����������ʿ����
