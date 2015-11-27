# RollViewPager
自动轮播的Viewpager

[中文](https://github.com/Jude95/RollViewPager/blob/master/README.md) | [English](https://github.com/Jude95/RollViewPager/blob/master/README_en.md)


触摸时会暂停播放，直到结束触摸一个延迟周期以后继续播放。
看起来就像这样。指示器可以为点可以为数字还可以自定义，位置也可以变。  
![example](example.jpg)

##依赖
`compile 'com.jude:rollviewpager:1.0.5'`

##xml属性
`app:rollviewpager_play_delay="3000"`  播放间隔时间，单位ms。填0则不播放。默认为0 
`app:rollviewpager_hint_mode="point"`  指示器展示模式,提供2种 `point`,`number`,默认不显示指示器  
`app:rollviewpager_hint_gravity="center"`  指示器位置,提供`left`,`center`,`right`。默认`center`  
`app:rollviewpager_hint_color="#7c7c7c"`  指示器背景颜色.默认黑色  
`app:rollviewpager_hint_alpha`="80"  指示器背景透明度。0全透明，255不透明。默认0.
`app:rollviewpager_hint_paddingLeft`="16dp"  指示器左边距
`app:rollviewpager_hint_paddingRight`="16dp"  指示器右边距
`app:rollviewpager_hint_paddingTop`="16dp"  指示器上边距
`app:rollviewpager_hint_paddingBottom`="16dp"  指示器下边距 
一般指定一下间隔时间和指示器类型就好了。

##Adapter
提供两种方便的PagerAdapter供使用。不仅用于本RollViewPager。任何ViewPager都可以。本ViewPager也可以使用其他任意PagerAdapter

####StaticPagerAdapter
存储页面的Adapter。view添加进去就存储不会再次`getView`，减少页面创建消耗，消耗内存。
概念参照FragmentPagerAdapter

####DynamicPagerAdapter
动态的Adapter。当创建3号view时会销毁1号view(递推)，会时常调用`getView`。增加页面创建消耗，减小内存消耗。
概念参照FragmentStatePagerAdapter  

License
-------

    Copyright 2015 Jude

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

       http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.
