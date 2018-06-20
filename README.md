# PKUSeg��һ����׼ȷ�ȵ����ķִʹ��߰�
PKUSeg�����ã�֧�ֶ�����ִʣ��ڲ�ͬ����������϶��������˷ִʵ�׼ȷ�ʡ�
## Ŀ¼
* [��Ŀ����](#��Ŀ����)
* [ʹ�÷�ʽ](#ʹ�÷�ʽ)
* [����ִʹ��߰������ܶԱ�](#����ִʹ��߰������ܶԱ�)
* [�������](#�������)
* [����](#����)

## ��Ŀ����

PKUSeg�ɱ�����ѧ���Լ��������ѧϰ�о��������Ƴ���һ��ȫ�µ����ķִʹ��߰���PKUSeg�������¼����ص㣺

1. ׼ȷ�ʸߡ�����ڴ�ͳ�ķִʹ��߰������ǵĹ��߰��ڲ�ͬ����������϶����ֳ��˸��õķִ�׼ȷ�ȡ�
1. ������ִʡ�����ѵ���˶��ֲ�ͬ����ķִ�ģ�͡����ݴ��ִʵ������ص㣬�û��������ɵ�ѡ��ͬ��ģ�͡�
3. ֧���û���ѵ��ģ�͡�֧���û�ʹ��ȫ�µı�ע�����ݽ���ѵ����

## ʹ�÷�ʽ
    * ����seg/bin/x64/ReleaseĿ¼�µ�seg.exe����windows�û���ֱ����cmd�����£�linux�����û���Ҫ����mono���
	* �ִ�ģʽ��[mono] LSTM.exe test [-input file] [-output file]
    * ѵ��ģʽ��[mono] LSTM.exe train [-train file] [-test file]
    * ���ı��ļ����������ע���ΪUTF8�ı���
### ����˵��
    test  �ִ�
    train ѵ��
    [-input] �û�ָ���Ĵ��ִ��ļ�
    [-output] �û�ָ���ķִʽ������ļ�
    [-trainFile] & [-testFile] �û���ע��ѵ�����ϣ�����֮���Ի��з��ָ�������֮���Կո�ָ�
    
### ��������
	mono LSTM.exe test data/input.txt data/output.txt 		linux�����½��зִ�
    LSTM.exe test data/input.txt data/output.txt 		windows �����½��зִ�
	mono LSTM.exe train data/train.txt data/test.txt 		����ָ����ѵ���ļ��Զ���ѵ����ѵ��ģ�ͻᱣ�浽seg/bin/x64/Release/modelĿ¼��
	
### Ԥѵ��ģ��
�ִ�ģʽ�£��û���Ҫ��seg/bin/x64/Release/model/fast����Ԥѵ���õ�ģ�ͣ����ݿ�����https://drive.google.com/open?id=1BxFoqHtieVzLnjOt1xfya6wR-voSUhA��ַ���أ����ݾ�����Ҫ���û������Զ����ѡ��ͬ��Ԥѵ��ģ�͡������Ƕ�ģ�͵�˵����

```
msra����MSRA���������ϣ���ѵ����ģ��
ctb8�� ��CTB8�������ı��������ı��Ļ�������ϣ���ѵ����ģ��
weibo����΢���������ı����ϣ���ѵ����ģ��
```
MSRA�����ɵڶ�����ʺ���ִ���������ṩ��http://sighan.cs.uchicago.edu/bakeoff2005/ ����CTB8��LDC�ṩ��https://catalog.ldc.upenn.edu/ldc2013t21   ����weibo������NLPCC�ִʱ����ṩ��http://tcci.ccf.org.cn/conference/2016/pages/page05_CFPTasks.html ����


## ����ִʹ��߰������ܶԱ�
����ѡ��THULAC����ͷִʹ��ڴ���ִ������LancoSeg�����ܱȽϡ�����ѡ��Windows��Ϊ���Ի���������������(MSRA)�ͻ�����ı�(CTB8)�����϶Բ�ͬ����������ٶȺ�׼ȷ�ʲ��ԡ�����ʹ���˵ڶ�����ʺ���ִ���������ṩ�ķִ����۽ű������������£�

MSRA

|Algorithm | Time | F-score|
|:------------|-------:|------------:|
| jieba | 0.82s |81.45 |
| THULAC | 7.12s | 85.48 |
| PKUSeg | 9.49s | 96.75 |

CTB8

|Algorithm | Time | F-score
|:------------|-------:|------------:|
|jieba|1.29s|79.58
|THULAC|5.15s|87.77
|PKUSeg|6.78s|95.64

## ��ԴЭ��
1. PKUSeg����������ѧ���о�������ҵ�Լ����������о�Ŀ����ѿ���Դ���롣
2. ���л���������⽫PKUSeg������ҵĿ�ģ��뷢�ʼ���xusun@pku.edu.cnǢ̸�������Э�顣
3. ��ӭ�Ըù��߰�����κα�������ͽ��顣�뷢�ʼ���jingjingxu@pku.edu.cn��

## �������
* Xu Sun, Houfeng Wang, Wenjie Li. Fast Online Training with Frequency-Adaptive Learning Rates for Chinese Word Segmentation and New Word Detection. ACL. 253�C262. 2012 
* Jingjing Xu, Xu Sun. Dependency-based Gated Recursive Neural Network for Chinese Word Segmentation. ACL 2016: 567-572

��ʹ�ô˹��߰����������������£�
```
@inproceedings{DBLP:conf/acl/SunWL12,
author = {Xu Sun and
Houfeng Wang and
Wenjie Li},
title = {Fast Online Training with Frequency-Adaptive Learning Rates for Chinese
Word Segmentation and New Word Detection},
booktitle = {The 50th Annual Meeting of the.pdf Association for Computational Linguistics, Proceedings of the Conference, July 8-14, 2012, Jeju Island, Korea- Volume 1: Long Papers},
pages = {253--262},
year = {2012}}

@inproceedings{DBLP:conf/acl/XuS16,
author = {Jingjing Xu and Xu Sun},
title = {Dependency-based Gated Recursive Neural Network for Chinese Word Segmentation},
booktitle = {Proceedings of the 54th Annual Meeting of the Association for Computational
Linguistics, {ACL} 2016, August 7-12, 2016, Berlin, Germany, Volume
2: Short Papers},
year = {2016}}
```
## ����

Xu Sun �����򣬵�ʦ��,  Jingjing Xu����������ʿ����
