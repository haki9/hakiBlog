---
date: "2019-03-20"
tags: ["android", "plugin"]
title: "Plugin with id 'com.github.dcendents.android-maven-plugin' not found"
---

## Problem

Plugin with id 'com.github.dcendents.android-maven-plugin' not found

## Fix

{{< code numbered="true" >}}
buildscript {
	repositories {
		jcenter()
	}
	dependencies {
		classpath 'com.github.dcendents:android-maven-gradle-plugin:1.5'
		classpath 'com.jfrog.bintray.gradle:gradle-bintray-plugin:1.7.3'
	}
}

apply plugin: 'com.android.library' apply plugin: 'com.android.library'
apply plugin: 'com.github.dcendents.android-maven' apply plugin: 'com.github.dcendents.android-maven'
apply plugin: 'com.jfrog.bintray' apply plugin: 'com.jfrog.bintray'
{{< /code >}}
