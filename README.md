# Windows ϵͳ��ʹ�� Claude for Desktop ����MCP���ӣ����������������ļ�
�������һ���� MCP Э�����Ӵ�ģ�͸����������ߵ������Ŀ�������Լ�ѧ��ѧ MCP Э�飬
�� Claude for Desktop ���˵����飬дƪ�������ܽ����������Լ��ȵ��Ŀӡ�<br>
���Ϲ��� MCP �ĸ�����ܵ�̫���ˣ�������Ͳ�д�ˡ��ɼ���ƪ�Ĳο����ף�[ʲô��MCPЭ�飿��ô�ã�һƪ������㵽��ͨ�Ľ̳̣������ClaudePro���ģ����ʹ��Claude3.7Sonnetģ�ͣ�](https://zhuanlan.zhihu.com/p/29820895586)<br>
## һ������ Claude for Desktop
���� Claude ����棬ֱ�ӽ���[���ع���](https://claude.ai/download)��ѡ�� Windows �� macOS ������ز���װ�����в�֧��Linux��
�ڹ����У����ܻ���ֱ���ֹ���ʵ����⣬��ʱ��Ҫ�����ӣ������ڵ������Ϊ������Ӣ�����й�����ĵ������й���۵Ľڵ�Ҳ���У�������
## �������� Python ����
Ϊ����δ�����й��ܵ���չ���ɰ�װ������ Python ���л��������汾�����3.9�����ϣ�
## ������װ Node.js
ʹ�õ��ļ�ϵͳ��������Ҫͨ�� npx ���� Javascript ģ�飬�����Ҫ��װ Node.js<br>
�ο�����һƪ<br>
[2025���°�Node.js���ذ�װ���������ý̳̣��ǳ���ϸ������������ŵ���ͨ��������һƪ�͹���](https://blog.csdn.net/jennycisp/article/details/144721124)
<br>
### 1.���ذ�װ��
���ʹٷ���վ��ַ[Download Node.js](https://nodejs.org/zh-cn/download/)��ѡ����Ҫ�İ汾���أ���ѡ�����Windows x64�ܹ����ٵ������Windows ��װ����
![alt text](image.png)
### 2.��װ
���Ű�װ�򵼵���ȥ����

![alt text](image-1.png)

���ݸ�������ѡ��װ·��

![alt text](image-2.png)

ֱ�Ӷ�ѡ��Ĭ�ϰ�װ

![alt text](image-3.png)

��ѡ���Զ���װ��Ҫ����

![alt text](image-5.png)

��� Install ���а�װ

![alt text](image-6.png)

��װ��Ϻ󣬲����Ƿ�װ�ɹ����� cmd �ն�������
```
node -v
npm -v
```
��������ʾ�汾��Ϣ��˵�� Node.js ��װ�ɹ�
### 3.��������
��1���ҵ���װ��Ŀ¼���ڰ�װĿ¼���½������ļ��С�node_global���͡�node_cache��
![alt text](����.PNG)

��2��������Ϻ�ʹ�ù���Ա��ݴ� cmd ����ڣ�����
```
npm config set prefix "���·��\node_global" ��������ոմ�����"node_global"�ļ���·����
npm config set cache "���·��\node_cache" ��������ոմ�����"node_cache"�ļ���·����
```
��3�����û�������
�١��˵��ԡ�-�����Ҽ�-�����ԡ�-���߼�ϵͳ���á�-������������
![alt text](image-7.png)

�� �ڡ�ϵͳ�������е�����½���
![alt text](image-8.png)
��������NODE_PATH
����ֵ��C:\Program Files\nodejs\node_global\node_modules
![alt text](image-9.png)
Ȼ����ͻᷢ�֡�node_global��������һ����node_modules���ļ���
![alt text](image-10.png)
Tips: ����������ֵ֮��û���Զ�������node_modules���ļ��У����ڡ�node_global�����ֶ�����һ����node_modules���ļ��У��ٸ����㴴���ġ�node_modules���ļ��е�·����ַ������ֵ

�۱༭���û��������еġ�Path��
![alt text](image-11.png)

�ܽ�Ĭ�ϵ� C ���¡� AppData\Roaming\npm ���޸ĳ� ��node_global����·�������ȷ��
![alt text](image-12.png)
![alt text](image-13.png)

���ڡ�ϵͳ��������ѡ��Path��������༭����ӡ�NODE_PATH�������һֱ�����ȷ����
![alt text](image-14.png)
![alt text](image-16.png)

### 4.����
���룺
```
npm install express -g   // -g����ȫ�ְ�װ
```
���������½����Ϊ���óɹ�
![alt text](����-1.PNG)

## �ġ�����ļ�ϵͳ MCP ������
�� Windows ϵͳΪ�������� Claude for Desktop ��������Ͻǣ��ҵ� Settings �����룬�ٽ��� Developer һ������� Edit Config
��������һ������ claude_desktop_config.json �ļ����ļ��У�������ļ������ļ������滻Ϊ��
```
{
  "mcpServers": {
    "filesystem": {
      "command": "npx",
      "args": [
        "-y",
        "@modelcontextprotocol/server-filesystem",
        "C:\\Users\\username\\Desktop",
        "C:\\Users\\username\\Downloads"
      ]
    }
  }
}
```
ȷ�� "C:\\Users\\username\\Desktop", "C:\\Users\\username\\Downloads" Ϊ��ϣ�� Claude �ܹ����ʺ��޸ĵ���ЧĿ¼����������Ϊ�������������������·��������Ҳ������Ӹ���·����
## �塢���� Claude ������
�����������ļ����������� Claude for Desktop
�ȴ�һ�����Ӧ�ûῴ�����������·�����һ������ͼ��![alt text](image-17.png)
������������ͨ�� Claude for Desktop �������ļ������޸�����ֻ���ڶԻ���������������еĲ�����Claude ������������ͬ����Զ������趨��·���µ��ļ����ж�Ӧ�ĸ��Ĳ���