This will be added into the samples later :)

For the to compile correctly you must do the following.

## From C++

1. IAP class must be called with
 
 ```java
	loadPlugin("IAPGooglePlay")
 ```
2. Item must be in google format like so
 ```java
	pInfo["IAPId"] = "com.game.example.item1" 

	// pInfo is of type TProductInfo
 ```
3. The developer info must be specific to your app like so
 ```java
	pPlayStoreInfo["GooglePlayAppKey"] = "Big long key from google :)"
	s_pPlayStore->configDeveloperInfo(pPlayStoreInfo);

	// s_pPlayStore is of type cocos2d::plugin::ProtocolIAP*
 ```


##From Java
```java
// This must be added to the new Cocos2dxActivity.java classes in cocos2d-x 3.0 + recently added

  @Override
  protected void onActivityResult(int requestCode, int resultCode, Intent data)
  {
    PluginWrapper.onActivityResult(requestCode, resultCode, data);
    super.onActivityResult(requestCode, resultCode, data);
  }
```
