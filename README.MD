# MoeGirlMidas

```
Version: 0.1
Author: Lei Mao
Updated: 8/9/2017
Institution: The University of Chicago
```

## Description

MoeGirlMidas is built on WikiMidas (https://github.com/leimao/WikiMidas) that I built previously for crawling the data from Wikipedia and MoeGirl APIs. MoeGirlMidas, however, is more specific to getting the fictional character articles and the character's properties from MoeGirl.

## Features

Search and retrieve for fictional characters' articles from MoeGirl (https://zh.moegirl.org/Mainpage).

## Dependencies

* re (https://pythonhosted.org/pyquery/)
* bs4 (https://www.crummy.com/software/BeautifulSoup/bs4/doc/)
* requests (http://docs.python-requests.org/en/master/)
* pyquery (https://docs.python.org/2/library/re.html)

## Usage

MoeGirlMidas was wrapped into a class object called "MoeGirlAPI". To use MoeGirlMidas in your Python program:

```python
from moegirlmidas import MoeGirlAPI
moegirl = MoeGirlAPI()
# To search for certain query in MoeGirl
# term is the keyword you are interested in; limit is the maximum number of returns
# the return is a list of relavant article titles found
search_result = moegirl.search(term = '���ѻ�֯', limit = 50)
for item in search_result:
    print(item)
>>>
���ѻ�֯

# To retrieve article from MoeGirl
# title is the title of the article you want to retrieve from MoeGirl
# the return is article-class object containing 'heading', 'summary', 'content', 'properties', 'image', 'references' and 'url'
article = moegirl.retrieve(title = '���ѻ�֯')
# To view the article content
print article.heading
>>>
���ѻ�֯

print article.image
>>> 
https://img.moegirl.org/common/thumb/f/fd/Kanzaki_Kaori.jpg/250px-Kanzaki_Kaori.jpg

print article.summary
>>>
���ѻ�֯����С˵��ħ������Ŀ¼��������������������������Ϸ����Ʒ�ĵǳ���ɫ��

print article.content
>>>
���ѻ�֯

���ѻ�֯ ����С˵��ħ������Ŀ¼��������������������������Ϸ����Ʒ�ĵǳ���ɫ��

Ŀ¼

������Ƭ

ְҵ��ħ��ʦ���׶�����ǰ5��

ħ������Salvere000�������⣺���޷�����֮�����Ԯ�֣�

������

Ӣ����̱�Ҫ֮��̻��ħ��ʦ��18�꣬�׶�����ǰ���ħ��ʦ�������ϲ���20λ��ʥ��֮һ�����ʽʮ����̵� Ů�̻� ������T-shirt��ţ�п�ĸ�� ���� ��Ů����ɱ���� ��ǧԪ ���������͡�Ψ������

��Ϊ�����Լ�ǿ����������Ὣ�޹������˾��룬һ��ѡ���뿪���ʽ��ӵ���š������������������֮�֡��Ĳ������񣬴Ӳ�ɱ�ˣ�Ҳ�����޷������������Լ���ǰ��ɱ��

���� ��β �� ��ɫ���� �������ʡ����ĸ��Ƥ��������Ů�����˺�����ò���ڵ����������ŹŴ� ��͸��� �ľ����Ը�����ע��������������ȫ��ѹ�ڳ����侲�ı���֮�¡�

���ϴ��������������T������ʱҲ������ţ�в������ף��������Ǵ���ţ�п㡣���������ֱ۵Ĳ��������һ���жϣ��෴�أ�ţ�п����Ǵ����ȸ�����ʼ��������е��� ���������� �� ���ߵ� �������ѵķ�װ�ܡ�ɫ�项��ʵ���ϣ����Ҳ��Գ�����Ϊ������ʽ����ϵ���Ҫ�����Ѳ����ǹ���Ҫ��¶�������ߡ� ������Ϊ��ǧԪ������������ˣ��º��ʾҪ�����岹���� �ڴ�������֮ǰ��鿴ħ������Ŀ¼���ص�

����֮��

����������Ĳ����������������һ���ӳ�����ʼ���൱���˵��ˡ�����ǰ�ͱ�ָ��Ϊ�����ʽʮ����̡���Ů�̻ʣ�ӵ�м�ʹ����Ŭ��Ҳ���Ի�óɹ��Ĳ��ܣ�ʲô���������Ϳ��Եõ�λ��Ⱥ�����ĵ��������ÿ�춼�ڷ��������Լ������ϲ����ľ�ϲ�������⵽��ɱ����Ҳ���Խ��Ҵ��ӵ���������ɵ���ƫ������ը�������߱�ը��Ҳ�����漣�Ƶغ������ˡ�

���ǣ������޷�ԭ���Լ�����Ϊ��Χ���������ҡ��ġ����ˡ���������Ϊ�����Լ�ǿ����������Ὣ�޹������˾��룬һ��ѡ���뿪���ʽ��Ϊ�˱������ߵ��ˣ�����ֻ��ѹ��ס���������һ������飬�Լ�ѡ���˹¶���

ħ����ʽ

����

���Ѳ���������˿��ʩչ����ն�����Կ��������ٶ�˺�Ѷ��֣�����ǰ��һ��ȫ�����������ѣ�����˵�Ƿǳ��ֲ�����ʽ������ʱ���ѵİε�����Ϊ�������β��ݸ�˿���֣���ʵ�������Ѹ���û�аε���ֻ�ǽ����ӵ�������΢�γ���Ȼ�����ƻ�ȥ���ˡ����ٶȿ�����һ˲��ɱ���ߴΣ��ʱ�������˲ɱ����
���á��������ĸ�˿����������޶ȵ�չ����ͨ�����ѿ��������Խ��и߿�����ʱ�ļ��١�

Ψ��

����ʹ�á������ߵ����İε�������ʮ�̵ֽ���ʽ���еĻ����÷����ʽ�������ʽ���еĻ����������ʽ�������ʽ���еĻ�����ʮ�ֽ���ʽ  ���������������ʵ������˴˵����㣬���ӳ���ȫ�ƻ����Ķ�һ�޶�������ʽ���ǡ�Ψ���������ض��ڽ��ػ�ʹ�������������ʽ������������һ��������ʹҲ���жϡ�
��Ψ��������˲��ʹ�á���֮�ӡ���������ʽ����Ϊ��ʥ�ˡ����ѿ���ʹ�ò��ֵġ���֮�ӡ�����������Ψ��������ʱ�����ѱ�ǿ���������������ᳬ�������ܲ��ݵ��˶��������Բ�����������״̬�³�ʱ�����ս����������ˣ����ѵġ�Ψ������Ҫ������һ�����ܾ�ʤ���İε���������Դ���ʹ����֮�����Ӱ��кͺ�֮ˮ��ʱ�򣬶���Ϊ��ʱ��ʹ����Ϊ��ʥ�ˡ���������ʹ������ٱ�����Ե  ��

�ⲿ������ע��

�����ģ� �ٷ�������ܣ� http://www.project-index.net/contents/hp0006/index00840000.html

�����˵�

for key in article.properties.keys():
    print key, ':', article.properties[key], '\n'
>>>
��ɫ : �ڷ� 

���Χ : ������� 

ͫɫ : ��ͫ 

���� : ���پ� 

�������� : Ӣ����̱�Ҫ֮��̻ᣬ���ʽʮ����� 

relatives : �������� �� ��ٿ�˿ �� ������˹ͼ���� �� ʷ���������Ŭ˹ 

�������� : �ձ� 

��� : ���ͷ 

���� : ���� �� ���󤶤� �� �� �� ������ �� ��Kanzaki Kaori�� 

���� : 18�� 

���� : 175cm���� 

�ȵ� : ����β �� ���� �� ���� ��ʥ�ˡ�Ů���ߡ� ��͸��� �������� 
```

The Python script could also be run directly in the shell (the shell might have conflicts with Chinese characters):

To search article
```shell
python moegirlmidas.py -s "���ѻ�֯"
```

To retrieve article
```shell
python moegirlmidas.py -r "���ѻ�֯"
```