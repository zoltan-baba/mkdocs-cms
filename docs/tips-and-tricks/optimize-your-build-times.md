# Optimize your build times

You can improve your build times with the following tips.

**Feel free to suggest other ways of optimization!**

## Include your dependencies in your repository

Including your dependencies \(like CocoaPods\) in your repository can speed up your builds. Once the `git clone` of your repository is done, everything will be in place to do your build.

For example, in case of CocoaPods, you can delete the CocoaPods Install step from your workflow if you include your `Pods` directory **and** the CocoaPods generated `.xcworkspace` file in your repository.

You can read more about the pros & cons of including your dependencies in your repository at: [Should I commit my dependencies into my repository?](https://github.com/OrganizationDummy/devcenter/tree/acf5f40e38b6dcf6fe62e839a4c04acb31fdebd2/faq/should-i-commit-my-dependencies-into-my-repository/README.md)

## Use the Build Cache

In some cases using the [Build Cache](https://github.com/OrganizationDummy/devcenter/tree/acf5f40e38b6dcf6fe62e839a4c04acb31fdebd2/caching/about-caching/README.md) feature can also help to speed up your builds. Note: the efficiency of the Build Cache depends on the size of the files you want to cache, as well as on the number of files you want to cache. For more information see the [Build Cache documentation](https://github.com/OrganizationDummy/devcenter/tree/acf5f40e38b6dcf6fe62e839a4c04acb31fdebd2/caching/about-caching/README.md).

## Turn off the "Clean build" option of Xcode steps

All of our Xcode steps \(Xcode Test, Xcode Archive and Xcode Analyze\) have a "Do a clean Xcode build ...?" option. You can usually turn off this option without causing any issues.

By turning off "clean build" you can speed up subsequent Xcode steps. The first one will still have to do a full, clean build, because there's no build cache at the time it runs \(as every build runs in a brand new, clean Virtual Machine, as descibed in [Code Security](https://github.com/OrganizationDummy/devcenter/tree/acf5f40e38b6dcf6fe62e839a4c04acb31fdebd2/getting-started/code-security/README.md)\), but subsequent Xcode steps can use the build cache of the previous Xcode step\(s\), reducing the compilation time of the step.

## Other

**Feel free to suggest other ways of optimization!**

* [Guarding Against Long Compiles](http://khanlou.com/2016/12/guarding-against-long-compiles/)

