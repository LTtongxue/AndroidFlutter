# AndroidFlutter
android原生混合Flutter,集成FlutterBoost

一、Android项目引入Flutter模块
1、app同级目录执行flutter create -t module honey_flutter
//2、cd honey_flutter/.android 运行 gradlew flutter：assembleDebug
3、app build.gradle中添加 
	compileOptions {
        sourceCompatibility 1.8
        targetCompatibility 1.8
    }
4、settings.gradle中添加 
	setBinding(new Binding([gradle: this]))
	evaluate(new File(
        'honey_flutter/.android/include_flutter.groovy'
	))
5、app build.gradle中添加 implementation project(':flutter')

二、添加FlutterBoost插件
1、pubspec.yaml中添加flutter_boost: ^0.0.411
