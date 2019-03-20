---
date: "2019-03-20"
tags: ["android", "module", "android studio 3.1", "pjsip"]
title: "Import new module to Android Project"
---

## Step 1. Download Module

   Unzip module after finish download

## Step 2. Import Module

Follow the following steps:

 1. File > New > Import Module 
 2. Choose Source Directory and Finish
 3. Go to Settings.gradle add **`include ':module_name'`**
 4. File > Project Structure > Dependencies > Add(+) 
 5. OR Add `implementation project(':sipservice')` in **build.gradle(App)**
