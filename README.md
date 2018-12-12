
# Chip View
This is a simple chip library that allows you to create your own chip views and views for the listview all within one adapter.

## Example

<img src="https://user-images.githubusercontent.com/35893133/49866793-c4e39500-fe2e-11e8-95de-d764cbebd91f.jpg" width="300">
<img src="https://user-images.githubusercontent.com/35893133/49866801-cca33980-fe2e-11e8-9c69-826c8b651e8a.jpg" width="300">
<img src="https://user-images.githubusercontent.com/35893133/49866806-d167ed80-fe2e-11e8-994b-9c5c1b787f02.jpg" width="300">
<img src="https://user-images.githubusercontent.com/35893133/49866818-d9279200-fe2e-11e8-8734-b4ebe9c46cb4.jpg" width="300">




## Download library with Jitpack.io
Add this to your build.gradle file for your app.
```java
	allprojects {
		repositories {
			...
			maven { url 'https://jitpack.io' }
		}
	}
```	

Add this to your dependencies in build.gradle for your project.
```java
	dependencies {
	        compile 'com.github.jakebonk:ChipView:1.0.1'
	}
```
## Usage
Create a ChipView in your xml file
```
  <com.allyants.chipview.ChipView
        android:id="@+id/cvTag"
        android:layout_width="match_parent"
        android:layout_height="match_parent"/>
```
Then in your Java code create and set the SimpleChipAdapter.

```java
ChipView cvTag = (ChipView)findViewById(R.id.cvTag);
        ArrayList<Object> data = new ArrayList<>();
        data.add("First Item");
        data.add("Second Item");
        data.add("Third Item");
        data.add("Fourth Item");
        data.add("Fifth Item");
        data.add("Sixth Item");
        data.add("Seventh Item");
        SimpleChipAdapter adapter = new SimpleChipAdapter(data);
        cvTag.setAdapter(adapter);
```
If you want to create your own adapter just extend the ChipAdapter class and use the SimpleChipAdapter class as a reference.
