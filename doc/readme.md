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
```dos
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
![](d1.png)
![](d2.png)
![](d3.png)
![](d4.png)
![](d5.png)
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
```cmd
:: ���¼ģʽ
::������Ϸ���������ݵ� Ĭ��Ŀ¼��Ĭ�ϻ���� depot �ֱ𹹽�Ŀ¼��ţ�
DepotDownloader.exe -app 904320
::������Ϸ�� ָ�� depot ����  ��Ĭ��Ŀ¼��Ĭ�ϻ���� depot �ֱ𹹽�Ŀ¼��ţ�
DepotDownloader.exe -app 904320 -depot 994710 904321

:: �������ԡ��Զ����� appid �����Դ���Ὣ��Դȫ������ apps/appid Ŀ¼��
DepotDownloader.exe -useAppDir -app 338930

::������Ϸ���������ݵ�ĳ��Ŀ¼
DepotDownloader.exe -app 904320 -dir E:/GameName
::������Ϸ�� ָ�� depot ���� ��ĳ��Ŀ¼
DepotDownloader.exe -app 904320 -depot 994710 904321 -dir E:/GameName

::ͨ��ָ���嵥������Ϸ (�嵥�ļ�Ҫ�ŵ� ��ǰ����� depotcache ��) depotId �� manifestId Ҫһһ��Ӧ
DepotDownloader.exe -app 534380 -depot 534381 -manifest 3462017367423786531 -useAppDir
DepotDownloader.exe -app 338930 -depot 338931 338932 347970 359000 359001 -manifest 1547401116504413409 3145636846994837120 7699221664155927697 2868566071607167109 761387674804236811 -useAppDir

::��¼ģʽ
::[������]ͨ���˺ź����� ���� ssfn ��¼ ��������Ϸ (ssfn�ļ�Ҫ�ŵ���ǰ����Ŀ¼)
DepotDownloader.exe -user �˺� -pass ���� -ssfn ssfnxxxxxx -app 904320 -depot 994710 904321 -useAppDir

::��½����ֻ��ȡ ������Կ���嵥
DepotDownloader.exe -user �˺� -pass ���� -ssfn ssfnxxxxx -app 904320 -manifest-only

::[������]ֻ��ȡ��Ϸ�嵥��Ϣ ���������ɽ����嵥(λ��depotcache_decryptĿ¼) (�����嵥Ӧ�ÿ���֧������Կ������Ϸ)
DepotDownloader.exe -user �˺� -pass ���� -ssfn ssfnxxxxxxxxxxxxxx -app 904320 -manifest-only -dm

::[������]����ָ����cdn
DepotDownloader.exe -app 904320 -cdn steampipe.akamaized.net:80,trts.baishancdnx.cn:80

::[������]ǿ��ͨ��depotid���أ��е���Ϸ app���������� �����޷��Զ���ȡ depot �б�
DepotDownloader.exe -app 338930 -depot 338931 338932 347970 359000 359001 -forceDepot
```
