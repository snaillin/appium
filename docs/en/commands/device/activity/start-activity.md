# Start Activity

Start an Android activity by providing package name and activity name
## Example Usage

```java
// Java
driver.startActivity(new Activity("com.example", "ActivityName"));

```

```python
# Python
self.driver.start_activity("com.example", "ActivityName");

```

```javascript
// Javascript
// webdriver.io example
driver.startActivity("com.example", "ActivityName");



// wd example
await driver.startActivity({
  appPackage: "com.example",
  appActivity: "ActivityName"
});

```

```ruby
# Ruby
@driver.start_activity app_package: "com.example", app_activity: "ActivityName"

```

```php
# PHP
$driver->startActivity(array('appPackage' => 'com.example',
                             'appActivity' => 'ActivityName'));

```

```csharp
// C#
// TODO C# sample

```



## Support

### Appium Server

|Platform|Driver|Platform Versions|Appium Version|Driver Version|
|--------|----------------|------|--------------|--------------|
| iOS | [XCUITest](/docs/en/drivers/ios-xcuitest.md) | None | None | None |
|  | [UIAutomation](/docs/en/drivers/ios-uiautomation.md) | None | None | None |
| Android | [UiAutomator2](/docs/en/drivers/android-uiautomator2.md) | ?+ | 1.6.0+ | All |
|  | [UiAutomator](/docs/en/drivers/android-uiautomator.md) | 4.2+ | All | All |
| Mac | [Mac](/docs/en/drivers/mac.md) | None | None | None |
| Windows | [Windows](/docs/en/drivers/windows.md) | None | None | None |

### Appium Clients

|Language|Support|Documentation|
|--------|-------|-------------|
|[Java](https://github.com/appium/java-client/releases/latest)| All |  [appium.github.io](http://appium.github.io/java-client/io/appium/java_client/android/AndroidMobileCommandHelper.html#startActivityCommand-java.lang.String-java.lang.String-java.lang.String-java.lang.String-java.lang.String-java.lang.String-java.lang.String-java.lang.String-boolean-)  |
|[Python](https://github.com/appium/python-client/releases/latest)| All |  [github.com](https://github.com/appium/python-client/blob/master/appium/webdriver/webdriver.py#L591)  |
|[Javascript (WebdriverIO)](http://webdriver.io/index.html)| All |  [webdriver.io](http://webdriver.io/api/mobile/startActivity.html)  |
|[Javascript (WD)](https://github.com/admc/wd/releases/latest)| All |  [github.com](https://github.com/admc/wd/blob/master/lib/commands.js#L2948)  |
|[Ruby](https://github.com/appium/ruby_lib/releases/latest)| All |  [www.rubydoc.info](http://www.rubydoc.info/github/appium/ruby_lib_core/Appium/Android/Device#start_activity-instance_method)  |
|[PHP](https://github.com/appium/php-client/releases/latest)| All |  [github.com](https://github.com/appium/php-client/)  |
|[C#](https://github.com/appium/appium-dotnet-driver/releases/latest)| All |  [github.com](https://github.com/appium/appium-dotnet-driver/)  |

## HTTP API Specifications

### Endpoint

`POST /wd/hub/session/:session_id/device/start_activity`

### URL Parameters

|name|description|
|----|-----------|
|session_id|ID of the session to route the command to|

### JSON Parameters

|name|type|description|
|----|----|-----------|
| appPackage | `string` | Name of the [package](https://developer.android.com/reference/java/lang/Package.html) |
| appActivity | `string` | Name of the [activity](https://developer.android.com/reference/android/app/Activity.html) |
| appWaitPackage | `string` | Automation will begin after this package starts |
| intentAction | `string` | [Intent](https://developer.android.com/reference/android/content/Intent.html) action which will be used to start activity |
| intentCategory | `string` | Intent category which will be used to start activity |
| intentFlags | `string` | Flags that will be used to start activity |
| optionalIntentArguments | `string` | Additional intent arguments that will be used to start activity |
| dontStopAppOnReset | `boolean` | Should the app stop on reset |

### Response

null

## See Also

* [JSONWP Specification](https://github.com/appium/appium-base-driver/blob/master/lib/mjsonwp/routes.js#L411)
