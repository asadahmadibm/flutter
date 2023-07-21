# flutter

یک فریم ورک که گوگل نوشته یه بار کد میزنیم و خروجی هر چی بخوایم در جد نیتیو میدهد

فلاتر از افزونه ها استفاده میکند 

در جاوا یا کاتلین افزونه ساخته میشود و در فلاتر از ان استفاده میکند


منحصر بفرد بودن فلاتر

خروجی نیتیو میدهد یعنی باینری کد نه جاوا یا کاتلین

پل ارتباطی نیاز ندارد


andriod command line tools

    flutter create my_app or flutter create .
    flutter run lib/main.dart
    flutter build apk --release
    output for windows C:\flutter2\build\windows\runner\Debug
    

# مهمترین فایلها
    lib/main.dart
    pubspec.yaml


in main.dart :

    import 'package:flutter/material.dart';
    
    void main() {
      runApp(const MyApp());
    }
    
    staeless myapp by st keyword

  
    MaterialApp(
          debugShowCheckedModeBanner: false,
          home: Scaffold(
            appBar: AppBar(
              backgroundColor: Colors.green,
              title:Text('toplearn'),
              centerTitle: true,
            ),
            drawer: Drawer(),
            floatingActionButton: FloatingActionButton(
              onPressed: (){},
              backgroundColor:  Colors.green,
              child: Icon(Icons.face),
            ),
          ) ,
        );
	
	
     setState(() {
    		  titleApp='hello title';
    		});	
    		
    width: double.infinity, کل عرض صفحه
# Widget Example    
    فاصله بین المان SizedBox(height: 20),
    Text('data',style: TextStyle(fontSize: 16,color: Colors.white)),
    ElevatedButton(onPressed: () { }, child: Text('کلیک کن'), style: TextButton.styleFrom(backgroundColor: Colors.white))
    

# add image or font
    1: add path in pubspec.yaml			
    2- use image.asset('assets/images/image1.jpg')
    
    add font
    1- add font in  pubspec.yaml	
    2-- add to MaterialApp(theme:ThemeData(fontFamily: 'iransans'),

# Goto Page    
    Navigator.push(context,
    MaterialPageRoute(
    	builder:(context){
    	return screen2();
    	})
    )
    or Get.Goto(screen2())
    
    Navigator.pop(context)
    
 # add package
    goto site : pub.dev & search package 
    1- add to dependency
    2- vpn and ctrl+s
    3- usage
    			
    			
  # store key value	with Shared Preferences
     
     import 'package:shared_preferences/shared_preferences.dart';
     
     final prefs = await SharedPreferences.getInstance();
     await prefs.setInt('num', 10);
     await prefs.setStringList('items', <String>['Earth', 'Moon', 'Sun']);
     
     await prefs.getInt('num');
     await prefs.getStringList('items');
