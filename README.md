# hasBrain_research
#XML declare
<EditText
     android:id="@+id/plain_text_input"
     android:layout_height="wrap_content"
     android:layout_width="match_parent"
     android:inputType="text"/>
# Java code
Field1 = (EditText)findViewById(R.id.field1);
Field1.addTextChangedListener(new TextWatcher() {
public void afterTextChanged(Editable s) {}

public void beforeTextChanged(CharSequence s, int start,
     int count, int after) {
   }
public void onTextChanged(CharSequence s, int start,
     int before, int count) {
      //Auto saveText here
   }
  });
#GetText :
EditText edittext=(EditText)findViewbyId(R.id.edittext);
String text = edittext.getText().toString;
#AutoComplete
?xml version="1.0" encoding="utf-8"?>
<AutoCompleteTextView xmlns:android="http://schemas.android.com/apk/res/android"
    android:id="@+id/autocomplete_country"
    android:layout_width="fill_parent"
    android:layout_height="wrap_content" />
@Java code :    
    // Get a reference to the AutoCompleteTextView in the layout
AutoCompleteTextView textView = (AutoCompleteTextView) findViewById(R.id.autocomplete_country);
// Get the string array
String[] countries = getResources().getStringArray(R.array.countries_array);
// Create the adapter and set it to the AutoCompleteTextView
ArrayAdapter<String> adapter =
        new ArrayAdapter<String>(this, android.R.layout.simple_list_item_1, countries);
textView.setAdapter(adapter);
    
    
     
     
     
