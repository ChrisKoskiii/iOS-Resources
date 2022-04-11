# Remove Storyboards

1. Delete the Main.storyboard and SceneDelegate files from the directory

 ![](https://github.com/ChrisKoskiii/iOS-Resources/blob/main/docs/assets/images/DeleteMain.png)

2. Using ⇧ ⌘ F, search for "Main"

 ![](/Users/christopherkoski/Desktop/searchMain.png)

3. Delete the Info.plist Values reference to Main

 ![](/Users/christopherkoski/Desktop/infoPlist1.png)

4. Delete the Application Scene Manifest

 ![](/Users/christopherkoski/Desktop/sceneManifest.png)

5. Delete everything in AppDelegate and replace with: 


	```
	import UIKit
	
	@main
	class AppDelegate: UIResponder, UIApplicationDelegate {
	  var window: UIWindow?
	  
	  func application(_ application: UIApplication, didFinishLaunchingWithOptions launchOptions: [UIApplication.LaunchOptionsKey : Any]? = nil) -> Bool {
	    
	    window = UIWindow(frame: UIScreen.main.bounds)
	    window?.makeKeyAndVisible()
	    window?.backgroundColor = .systemBackground
	    window?.rootViewController = ViewController()
	    
	    return true
	  }
	}
	```


