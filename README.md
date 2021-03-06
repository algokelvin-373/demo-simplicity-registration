<h1 align="center">Demo 'The Simplicity of Registration'</h1>

<p align="center">
  <a href="https://jitpack.io/#kelvin373-ht/simplicity-registration"><img alt="bintray" src="https://jitpack.io/v/algokelvin-373/simplicity-registration.svg"></a>
  <a href="LICENSE"><img alt="License" src="https://img.shields.io/github/license/algokelvin-373/demo-simplicity-registration"></a>
  <a href="https://github.com/algokelvin-373"><img alt="Github" src="https://img.shields.io/github/followers/algokelvin-373?label=follow&style=social"></a>
  <a href="https://www.youtube.com/c/AlgoKelvin373/"><img alt="Youtube" src="https://img.shields.io/youtube/channel/views/UCpSHZFRx64xWwXYbWbyXxfw?style=social"></a>
  <a href="https://www.youtube.com/c/AlgoKelvin373/"><img alt="Youtube" src="https://img.shields.io/youtube/channel/subscribers/UCpSHZFRx64xWwXYbWbyXxfw?style=social"></a>
</p>

<p align="center">The Simplicity Registration of Android</p>

## Description

The Simplicity of Registration

## Demo Program

Coming Soon

## _Step by Step to implement this_

#### 1. Add the JitPack repository to your `build.gradle`

```gradle
allprojects {
    repositories {
        ...
        maven { url 'https://jitpack.io' }
    }
}
  ```
  #### 2. Add Module dependency in your `app/build.gradle`
  
  ```gradle
  dependencies {
    implementation 'com.github.kelvin373-ht:simplicity-registration:1.0.0'
  }
  ```
  #### 3. Extends class `TabPageLayer` in MainActivity
  ```java
  public class MainActivity extends TabPageLayer {

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);

        ...

    }
}
  ```
  #### 4. Set `setTabPageLayer`, `setPageDetailData`, and `setPageEnds`
  ```js
  public class MainActivity extends TabPageLayer {

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);

        // Set All Fragments
        Fragment[] fragments = {new PageOneFragment(), new PageTwoFragment(), new PageThreeFragment()};
        
        // Set countData, id tablayout, id viewpager, and fragments
        setTabPageLayer(9, R.id.tabHome, R.id.viewPager, fragments);
        
        // Set name class to show data register
        setPageDetailData(DataRegisterActivity.class);
        
        // Set page end
        setPageEnds(fragments.length);

    }
}
  ```

### Contributions

Any contributions are welcome. You can send PR or open issues.
Thank you

### LICENSE
```
MIT License

Copyright (c) 2021 Algokelvin

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```
