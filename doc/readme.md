## ����  
��ǰ����Steam��Դ�ȽϷ��㣬����Steam�����嵥����֮�󣬾ͱ���ӵ����Ϸ�����õ�Steam���嵥��  
Ȼ�� �и����� **[wxy1343](https://github.com/wxy1343)** ��ͨ���ռ�һЩ��������ߺ�����ȡ�ռ��嵥��  
ͨ����Щ�嵥 ���Դ� Steam ��cdn��ֱ������������������ٱ� �����Ӻ��������Ŀ죨Ӧ��...��  
���� ֻ��������� ��������ô�죿 ����ɻ�Ա���Լ���취��~  
���� tools С���� ģ���� less ��...   

## ManifestDownload ��Steam�嵥��������
### ��������ͼ  
![](m1.png)
![](m2.png)

### ����˵��  
�嵥������Դ��**[ManifestAutoUpdate](https://github.com/wxy1343/ManifestAutoUpdate)**  
ͨ�� Steam �� appid ����ȡ app ��Ӧ���嵥�б����£�������ֿ�������¼�Ļ���  
��ǰ��¼ [�����ĵ�](https://docs.google.com/spreadsheets/d/1tS-Tar11TAqnlaeh4c7kHJq-vHF8QiQ-EtcEy5NO8a8)  
Steam �� appid ��β鿴��
�ͱ��� ���8 ��ͨ�� Steam�̵� �� Steamdb ���Կ�������
```
https://store.steampowered.com/app/1196590/Resident_Evil_Village/  
https://steamdb.info/app/1196590/  
```
�Ǹ� 1196590 ���� appid

����ϸ�ڿ������о�  
��Ϊ�Ƿ���GitHub��api��ȡ���ݣ�����GitHub�� Api ��������Ƶ�����ơ�  
��token��60��/Сʱ  
��token��5000��/Сʱ  
���� �б�Ҫ ������GitHub������һ�� ��Ȩ�޵� Person Token �ŵ������ļ��С�

������� ��Ȼ����ʹ����û���ֱ� qiang ����������� ���ų���һ...  
�����һ�Ļ������������о�ʹ��ħ��...  

**Ps.���������ûɶ��������������Ϊ���ⱻ�޸��İ�����Ϊ X�� X�� ��Ĳ�����ߣ���򵥼Ӹ��ǡ�**

### ���߲���
```shell
::����appid ������Դ�嵥
ManifestDownload.exe app [appid1 appid2]
ManifestDownload.exe app 1000
ManifestDownload.exe app 1000 2000

::����manifest ���� ָ�����嵥��һ�����ò���
ManifestDownload.exe manifest [manifestId1 manifestId2]
ManifestDownload.exe manifest 4004_2300048559188578691

::��ȡ�������嵥�����еĽ�����Կ��app����ʱ���Զ���ȡ��DepotDownloader��������
ManifestDownload.exe dumpkey
```

## DepotDownloader��ħ�ģ� Steam��Դ������
### ��������ͼ

### ����˵��
������ħ���� **[SteamRE/DepotDownloader](https://github.com/SteamRE/DepotDownloader)**  
����һЩ��ݹ��ܣ�����
* ֧�����¼����  
* ����Steamԭʼ�嵥
* ��������嵥
* �Զ�ʶ�𱾵������嵥
* ֧��ָ��ssfn 
* ��Ӷ��� cdn ������
* �޸����� cdn �������Ƶ������

�������ϸ�� ��ʹ�÷��� �ο�ԭ��Ŀ ReadMe��  
Ϊ�˰�ȫ�������Ȼ����Ŀ֧��ͨ���˺������ȡ�嵥��������Դ���� **���Ƽ�ʹ���Լ����˺�**  
���б�Ҫʹ���˺�ģʽ���Ƽ�ʹ�� **���ߺ�** �� **�����** ȥ���ء�

**Ps.�������Ȼ��ħ�������ο�ԴЭ��ΪGPL2������Ϊ���ⱻ�޸��İ�����Ϊ X�� X�� ��Ĳ�����ߣ���򵥼Ӹ��ǡ�**

### ���߲�������ħ�ĺ������ԣ�
```shell

```
