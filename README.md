# PickerView-Android
<img src="https://raw.githubusercontent.com/tusinh/PickerView-Android/master/img.png" width="300" height="600" />

# How to Use
* add PickerView like your module lib android.
1. init global
 ```java
 MyOptionsPickerView singlePicker;
 ```
 
2. setData String 
```java
    //Single String Picker
        singlePicker = new MyOptionsPickerView(MainActivity.this);
        final ArrayList<String> items = new ArrayList<String>();
        items.add("A");
        items.add("B");
        items.add("C");
        items.add("D");
        items.add("E");
        singlePicker.setPicker(items);
        singlePicker.setTitle("Single Picker");
        singlePicker.setCyclic(false);
        singlePicker.setSelectOptions(0);
        singlePicker.setOnoptionsSelectListener(new MyOptionsPickerView.OnOptionsSelectListener() {
            @Override
            public void onOptionsSelect(int options1, int option2, int options3) {
                //  singleTVOptions.setText("Single Picker " + items.get(options1));
                Toast.makeText(MainActivity.this, "" + items.get(options1), Toast.LENGTH_SHORT).show();
//                vMasker.setVisibility(View.GONE);
            }
        });
```
3. show 
```java
   singleTVOptions.setOnClickListener(new View.OnClickListener() {

            @Override
            public void onClick(View v) {
                singlePicker.show();
            }
        });
```
