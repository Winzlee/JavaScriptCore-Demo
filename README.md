JavaScriptCore-Demo
===================

JavaScriptCore.framework ：iOS7 中新加入的框架，用来处理JavaScript。JavaScriptCore 是苹果 Safari 浏览器的 JavaScript 引擎，JavaScriptCor在 OS X 平台上很早就存在的，而在 iOS 平台，直到IOS7才对外开放，并提供了 Objective-C 的接口

====================
Edited by Winzlee
注：在JSCallOC中，当创建原生的UIAlertView的时候，需要把代码放到主线程中，否则就会因为在后台修改了视图而抛出异常，会在以后的操作中有影响。
        [[NSOperationQueue mainQueue]addOperationWithBlock:^{
            
            UIAlertView *alert = [[UIAlertView alloc]initWithTitle:@"提示" message:str delegate:nil cancelButtonTitle:@"确定" otherButtonTitles:nil, nil];
            [alert show];
        }];
