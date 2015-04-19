# AndroidFontStyleFactory
An Easy Way For Android Developers To Set Font Styles for TextViews

This Small Piece of development should assist developers in setting typefaces for TextView/TextViews and also take off the 
stress of always trying to Call on <code>Typeface.createFromAsset(....);</code> on every <code>Textview</code> 
or an Instance of TextView e.g Buttons.

To set the TypeFace for a particular TextView instance all you need do is :

<code>
	TextView myTextView = (TextView) findViewById(R.id.myText);
</code>

<code>
	FontStyleFactory.setFontForView(context, myTextView, StyleConstants.GENERAL_APP_FONT);
</code>


To set the TypeFace for a group of TextView instance all you need do is :

Initialize all Your TextView Instance First.

<code>
		setHbFirstName((EditText)findViewById(R.id.hb_sign_up_first_name));
        setHbLastName((EditText)findViewById(R.id.hb_sign_up_last_name));
        setHbEmailAddress((EditText)findViewById(R.id.hb_sign_up_email));
        setHbMobileNumber((EditText)findViewById(R.id.hb_sign_up_mobile));
        setHbPassword((EditText)findViewById(R.id.hb_sign_up_password));
        setHbSignUpBtn((Button)findViewById(R.id.hb_sign_up_btn));
        setHbSex((Spinner)findViewById(R.id.hb_sign_up_sex));
        setHbDateOfBirth((EditText)findViewById(R.id.hb_sign_up_dob));
        setHbAddress((EditText)findViewById(R.id.hb_sign_up_address));
</code>

<code>
		View[] views = {hbFirstName, hbLastName,hbEmailAddress, hbMobileNumber, hbSignUpBtn, hbPassword,hbSex, hbDateOfBirth, hbAddress};
	
		FontStyleFactory.setFontForAllViews(this, views, StyleConstants.GENERAL_APP_FONT);
</code>


<b>NOTE</b>

The StyleConstants should only contain <code>static String</code> <i style="color:blue">variable</i>
which holds values of a TFF (font files) file name in the android asset directory.
