ȫ�ְ�װ
webpack
cli�����ּܣ�
npm(cnpm) install webpack webpack-cli -g
�ֲ���װ webpack
npm init
npm��cnpm��install webpack webpack-cli --save
Ĭ�ϲ���
���(entry):./src/index.js
���� (output):./dist/main.js
ѹ����δѹ����
webpack --mode development 
webpack --mode production ѹ��
�Զ���
�� package.json->script->����һ����ֵ
���� ��npm run ָ�������
���ط���
webpack-dev -server
��װ���ط��� npm (cnpm) install webpack-dev -server --save
��webpack.config.js->devServer->contentBase����webpack���·����
���html�ļ�
��װhtml-webpack-plugins npm(cnpm) install html-webpack-plugin --save
��webpack.config.js->����html-webpack-plugin->����plugins->ʵ����һ��htmlwebpackplugins(template:"��Ҫ�����html�ļ�·��./src/index.html")
���css�ļ��Լ������ļ�
loader���س���
����css�ļ�->����npm(cnpm) install css-loader style-loader --save
ts-loader typescripts