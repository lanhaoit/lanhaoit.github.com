---
layout: post
title: "设计模式-观察者模式"
description: ""
category: "program"
tags: [设计模式]
---
### 目录文件

[TOC]

### 气象观油站
我们的工作是利用WaetherData对象取得数据，并更新三个布告板：目前状况、气象统计和天气预报。
> 设计思路1：
> -WeatherData类具有getter方法，可以取得三个测量值：温度、湿度与气压]
> -数据改变，measurementsChanged()方法就会被调用
> -**此系统必须可扩展，可以添加或删除布告板

### 定义观察者模式
> 定义观察者模式：
> 定义了对象之间的一对多的依赖，这样一来，当一个对象改变状态时，它的所有依赖者都会收到通知并自动更新
> 有点像读者与出版社的关系，只要你有在报社订阅，它有新的报纸就会给你派送

### 松耦合的威力
当两个对象之间松耦合，它们依然可以交互，但是不太清楚彼此的细节。
观察者模式提供了一种对象设计，让主题和观察者之间松耦合。

> 设计原则：
> 为了交互对象之间的松耦合设计而努力
松耦合的设计之所以能让我们建立有弹性的OO系统，能够应对变化是因为对象之间的互相依赖降到了最低

### 实现气象站
#### 建立接口
```
public interface Subject {
    public void registerObserver(Observer o);
        public void removeOberver(Observer o);
            public void notifyObservers();
            }

public interface Observer{
    public void update(float temp, float humidity, float pressure);
    }

public interface DisplayElement {
    public void display();
    }
    ```
    #### WeatherData类中实现主题接口

#### 建立布告板

#### 启动气象站

### 使用Java内建的观察者模式
Observer有两种实现方式，一种就是刚说的在通知更新的时候，就信息更新给订阅用户。
另一种是用户通过getter方法获取

Java内部是另一种实现Observer的方式
> 比较：
> 1.
> 2.
