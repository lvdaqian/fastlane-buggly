# fastlane-buggly
A fastlane action to upload the dSYM file to buggly which is a crash analyze system.

**Note**: This project is still in development.

# Installation

Clone the repo. and copy the fastlane folder to your project root folder.

# Basic usage

Just add the action `upload_to_buggly` to your lanes.

sample code:

```ruby 
lane :beta do
	increment_build_number 
	gym
	upload_to_buggly(appId:your_buggly_app_id,
					appKey:your_buggly_app_key)
end
```

You can found your buggly app id and app key when you register your app in buggly. For more infomation about buggly see: https://bugly.qq.com
 
You can also set the buggly app id and app key in the Appfile.

Appfile:

```ruby
app_identifier "xxx.xxx.xxxx" # The bundle identifier of your app
apple_id "xxxx@xxxx.com" # Your Apple email address

buggly_app_id "your_buggly_app_id"
buggly_app_key "your_buggly_app_key"
```
 
More Reference can be shown by following command.

```shell
fastlane action upload_to_buggly
```
