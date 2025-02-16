This Tool is selected as 
[BlackHat Arsenal USA 2020](https://www.blackhat.com/us-20/arsenal/schedule/#deoptfuscator-automated-deobfuscation-of-android-bytecode-using-compilation-optimization-19958)

## What is Deoptfuscator

+ Deoptfuscator is a tool for deobfuscating Android applications that have been transformed using control-flow obfuscation mechanisms.
+ Deoptfuscator can reverse the control-flow obfuscation performed by DexGuard on open-source Android applications.

## Prerequisites
In order to build and run deoptfuscator, the followings are required:

+ Deoptfuscator based on Ubuntu 18.04 LTS 64bit PC
  + libboost, libjson (C++ library)
    ```
    $ sudo apt-get install libboost-all-dev  
    $ sudo apt-get install libjsoncpp-dev
    ```
  + openjdk
    ```
    $ sudo apt-get install openjdk-11-jdk
    ```
  + i386 libc
    ```
    $ sudo dpkg --add-architecture i386  
    $ sudo apt-get update  
    $ sudo apt-get install libc6:i386 libstdc++6:i386
    ```
  + zipalign
    ```
    $ sudo apt-get install zipalign
    ```
  + apksigner
    ```
    $ sudo apt-get install apksigner
    ```
## How to Install
 + deoptfuscator's repositary need git-lfs
  + Git LFS
  ```
  $ curl -s https://packagecloud.io/install/repositories/github/git-lfs/script.deb.sh | sudo bash
  $ sudo apt install git-lfs
  $ git clone https://github.com/Gyoonus/deoptfuscator.git
  ```

Our repository Already Contains Tools needed to run our Tool
 + Apktools : [https://ibotpeaches.github.io/Apktool/](https://ibotpeaches.github.io/Apktool/)
 + fbredex : [https://fbredex.com/](https://fbredex.com/)


## HOW TO USE
+ Set Local Environment  
  ``` 
  $ . ./launch.sh  
  ```
    OR
  ```
   $ source ./launch.sh
  ```

+ Deobfuscate an Android application that has been transformed using control-flow obfuscated techniques.  
  ```
  $ python3 deoptfuscator.py <obfuscated_apk>  
  ```
+ Test our tools!  
  ```
  $ python3 deoptfuscator.py test/AndroZoo_DexGuard_apk/com.alienguns.scifirifles_4F326C99558145BB636D31C96488823A.apk
  ```
  + If the input file (an obfuscated app) was `com.alienguns.scifirifles_4F326C99558145BB636D31C96488823A.apk`, the file name of the deobfuscated apk is `com.alienguns.scifirifles_4F326C99558145BB636D31C96488823A_deobfuscated_align.apk`
  + There is a problem with the license, so we stop sharing the test app for a while.

+ Our tool can effectively deobfuscate Android applications transformed with the control flow obfuscation option of DexGuard :
  + Our tool can currently handle the control-flow obfuscation techniques of DexGuard.
  + It cannot handle other obfuscation techniques such as layout obfuscation, identifier renaming, and string encryption.
![git](https://user-images.githubusercontent.com/64211521/100713131-2542b700-33f7-11eb-87f5-968d5eb13563.png)

## Contact
+ E-mail : gyoonus at gmail dot com [Gyoosik Kim(김규식)]
+ Mobile : 082)10-9888-2792

## Acknowledgement

+ This research was supported by Basic Science Research Program through the National Research Foundation of Korea(NRF) funded by the Ministry of Science and ICT (no. 2018R1A2B2004830)
![시그니처 가로형_영문조합형](https://user-images.githubusercontent.com/64211521/80204259-7e798980-8663-11ea-95f1-ff19ccb86a77.jpg)

