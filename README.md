# Logging

Logging.dll ����� ��� ������ ����� � ����� � ���� ������. 
����� LogToFile ����� ��� ������ ����� � ����� ��������.
����� �������� ���������, ��� ��� ������������� ��������� ������� ��������� ������.
��� �������� ���������� ������ ����� ��������������� ������������� �� ���������.
___
������:
```csharp
private LogToFile log = new LogToFile();  
```
��� ������������� ������������ �� ��������� ������������ ������ `LogConfig.cfg`. � ������� ������� ����, ��� ����� ��������� ����� � ����������� �����.
___
���� �� ���������:
```
ErrorPath=Logging//Error.log
InfoPath=Logging//Info.log
WarningPath=Logging//Warning.log
FatalPath=Logging//Fatal.log
SuccesPath=Logging//Success.log  
```
___
��� �� ��� �������� ���������� ������ ����� ��������������� �������������, ��� ����� �������������� ��������� ���� � ������ �����.
___
������:
```csharp
private LogToFile log = new LogToFile(errorPath, infoPath, warningPath, fatalPath, successPath);
```
___
��� ������ � ��� ����� ������������ ������� �������: Info, Error, Warning, Fatal � Success. ��� ������� ���������, ��� ������ ���� ��������� �������� ���� string.
___
������:
```csharp
private LogToFile log = new LogToFile();  
log.Info("����������");
```
___
����� ������� � ����� ���� Info.log ������ ����� ��������� ��������� �������:
```
11:34:00 [INFO] : ����������
```
___
������ ������� ����� ������������ ������� Log, ���� ��������� ��� ��������� ���� string.
___
������:
```csharp
private LogToFile log = new LogToFile(); 
private string path = @"Logging\Other.log"; 
private string type = "OTHER";
private string message = "����� ���������";
log.Log(path, type, message);
```
___
��� ������ � ����� Other.log ����� �������� ���������:
```
11:34:00 [OTHER] : ����� ���������
```
___