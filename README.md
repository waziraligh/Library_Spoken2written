# Library_Spoken2written


This is a library which converts a paragraph of spoken english to written english on a static set of rules which are actually fixed and are written in the .py file which is the library.

#### Implemented Features:-

1) Conversion of a number between one to hundred in text to it's corresponding integer.
2) Conversion of words such as C M, P M, A M, D M and H T M L to words CM, PM, AM, DM and HTML respectively.
3) Conversion of phrases such as triple A, quadrapule B, double C to AAA, BBBB and CC respectively.
4) Conversion of two dollars to $2, three dollars to $3 and so on. Please note that the handling of twenty one to twenty nine dollars, thrity one to thrity nine dollars and so on in every tens has not been handled starting from twenty one.

#### Important feature but yet to implement:-

Features which are important but are yet to be implemented are the dynamic set of rules which would essentially mean that the user can update a rule for converting a phrase in spoken english to written english dynalically while using the library through a method of the library.
rom 
#### Instructions for using code as a library:-

1) This library is named as Spoken2Writtenenglish.py which can be imported using the import command in python in any other program.
2) It has the class conversion which has two methods __init__ which takes an input of the object of the class itself and convert which takes inputs as objects of the class and the paragraph of spoken english which needs to be converted. 
3) The class conversion's method convert does the conversion of the spoken english paragraph and prints out the input paragraph and the output paragraph at the end.
4) There are a couple of other functions defined in the library itself which are conversion_rules and word_check.

   a) Conversion_rules function doesn't take any argument. It defines a static set of rules for the purpose of conversion of spoken English to written English and returns the         rules to the calling function.
   
   b) word_check function takes a word as an input and returns only the word if the word doesn't contain commas and full-stops otherwise it returns the actual word along with         comma and/or full stop.
5) In the calling program, wherein the class conversion from the library Spoken2WrittenEnglish is imported, an instance of the class conversion of the library needs to be created and the method convert needs to be called using the command object_instance.convert(). After that the output would be the input paragraph followed by the output converted paragraph.

#### Instructions for using the REST API on a local machine:-

1) As known, REST API is an interface around a function or a model which can be used to handle requests from the model from a remote box or from the client side. I have used FLASK API in this project.
2) I have this app.py which is a python file that contains the class conversion and the two functions and the two functions Conversion_rules and word_check. This app.py file also handles the requests from an HTML form whenever the submit button is pressed in the form. On pressing the button submit, it would trigger the predict function. The app.py file whenever called runs the application on the port 8080 on a local host.
3) The predict function calls the class conversion and creates an object of the same and then calls the method convert with the paragraph collected from the HTML form through the submit button over there.
4) The output of the convert method is returned as a json file in the form a dictionary which has the key as Written English Paragraph and the value as the converted paragraph.
5) A simple form named index.html is created which takes the Spoken English paragraph from the user. This html file is saved in the folder template.
6) For running the REST API, please open command prompt and change the directory to the folder where the app.py and template folders are present.
7) In the command prompt, please type python3 app.py which would show you the informations related to the port where this application is running.
8) Now, open up your web browser and paste the ip address with the port from your command prompt and then type /index in the address bar following the ip address and the port      number.
9) This will open up the form which would have a text box for entering the spoken english paragraph along with the submit button.
10) Please enter the paragraph and press submit button. You would be redirected to the next page which would give an output in the form of dictionary with the key Written English Paragraph and the value as the converted paragraph in Written English.

#### Uploads:-

1) Library - Spoken2Writtenenglish.py which can be imported from other .py files
2) Background application running for the REST API - app.py
3) HTML form - The .zip folder templates.zip which needs to be unzipped and saved in a folder templates which would contain the index.html file that would be opened up in a        browser when app.py would be run from the command prompt.

