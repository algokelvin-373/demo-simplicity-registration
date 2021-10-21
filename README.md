<h1 align="center">Demo 'The Simplicity of Registration'</h1>

<p align="center">
  <a href="https://jitpack.io/#kelvin373-ht/simplicity-registration"><img alt="bintray" src="https://jitpack.io/v/kelvin373-ht/simplicity-registration.svg"></a>
  <a href="LICENSE"><img alt="License" src="https://img.shields.io/github/license/kelvin373-ht/demo-simplicity-registration"></a>
  <a href="https://github.com/kelvin373-ht"><img alt="Github" src="https://img.shields.io/github/followers/kelvin373-ht?label=follow&style=social"></a>
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
  #### 5. Extends Class `RegisterController` in all your fragment
  ```js
  public class PageOneFragment extends RegisterController {

    @Override
    public View onCreateView(LayoutInflater inflater, ViewGroup container, Bundle savedInstanceState) {
        return inflater.inflate(R.layout.fragment_page_one, container, false);
    }

    @Override
    public void onViewCreated(@NonNull @NotNull View view, @Nullable @org.jetbrains.annotations.Nullable Bundle savedInstanceState) {
        super.onViewCreated(view, savedInstanceState);

        ....

    }
}
  ```
  #### 6. Set `setSizes`, `setUIRegister`, and `setBtnNext` for fragment AND Set xml linear layout
  _PageOneFragment_
  ```js
  @Override
    public void onViewCreated(@NonNull @NotNull View view, @Nullable @org.jetbrains.annotations.Nullable Bundle savedInstanceState) {
        super.onViewCreated(view, savedInstanceState);

        // Set Title Text Input Data
        String[] text = {"Nama Lengkap", "Nama Panggilan", "Tempat Lahir"};
        
        // Set Hint EditText
        String[] edtHint = {"Nama Lengkap", "Nama Panggilan", "Tempat Lahir"};
        
        setSizes(text.length); // Set Amount Input Data
        
        // Set parameter view, array title input data, and array hint text
        setUIRegister(view, text, edtHint, R.id.cl_register_1);
        
        setBtnNext(R.id.btn_next); // Set id Button Next

    }
  ```
  _fragment_page_one.xml_
  ```xml
  <androidx.constraintlayout.widget.ConstraintLayout
        android:layout_width="match_parent"
        android:layout_height="match_parent">

        ....

        <LinearLayout
            android:id="@+id/cl_register_1"
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:layout_marginTop="8dp"
            android:layout_marginStart="8dp"
            android:layout_marginEnd="8dp"
            android:orientation="vertical"
            app:layout_constraintEnd_toEndOf="parent"
            app:layout_constraintStart_toStartOf="parent"
            app:layout_constraintTop_toBottomOf="@+id/txt_fragment_one" />
            
        ...    

    </androidx.constraintlayout.widget.ConstraintLayout>
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
