Download Link: https://assignmentchef.com/product/solved-ista-130-programming-assignment-9-lists-and-dictionaries
<br>
<strong>1.0)  FISH CATCH (40 POINTS) </strong>

<strong> </strong>

<h1>1.1)  DETAILS</h1>

<strong> </strong>

Download the plain text files “fishcatch.txt” and “fishcatch.dat” from D2L and open them both with Sublime, Notepad++, or any plain text editor.

The “fishcatch.txt” file gives an explanation of the data contained in the “fishcatch.dat” file. Read the explanation to understand what is in the “fishcatch.dat” file.  For this assignment we’ll only be interested in the name and weight of each fish in the “.dat” file.




Create a new file called “fishcatch.py”. In the file:




<ul>

 <li>Write a function called <strong>fish_dict_from_file</strong> that takes a single string parameter giving the name of a file to read.</li>

</ul>




i.) In the function make a literal dictionary containing the mapping from the  Numeric Species Code to the English fish name.

<ul>

 <li>For example, in your literal dictionary the key 1 will map to the value “Bream”. If your literal dictionary is called fishmap then the following expression would be True: fishmap[1] == “Bream”.</li>

 <li>You’ll use this dictionary in the next step to get the name of each fish.</li>

</ul>




ii.) Next create an empty dictionary and read each fish Species and Weight from  the “fishcatch.dat” file into the dictionary, mapping the English name of each  fish species onto a list containing the weights of all of the fish of that type that were  caught. • i.e. for each different fish name the dictionary will contain a single list of floats.

<strong>–</strong> e.g. the dictionary will have one <strong><em>key-value</em></strong> pair for “Bream”. The key will be “Bream” and the value will be a list of floats containing the weights of all of the Bream that were caught.

<ul>

 <li>Skip any fish that has a missing weight value (i.e. weight is “NA”).</li>

</ul>




iii.)  Return the dictionary that contains the fish names and weights.




<ul>

 <li>In <strong>main</strong>:</li>

</ul>




<ul>

 <li>Call your function to get a dictionary of fish names and weights.</li>

</ul>




<ul>

 <li>Print a report showing for each fish the number of fish of that type, the name          of the fish, and the mean weight of that fish type in grams.

  <ul>

   <li>The report should show the fish in alphabetical order.</li>

   <li>Make it pretty as shown in the following example:</li>

  </ul></li>

</ul>




# NAME           MEAN WT

11 ?                154.8g

34 Bream            626.0g

56 Perch            382.2g          17 Pike            718.7g           20 Roach            152.1g            14 Smelt             11.2g           6 Whitefish        531.0g




<u>NOTE</u>:  You will need to right justify the <strong>#</strong> by 4, left justify the <strong>NAME </strong>by                           10 and finally right justify the <strong>MEAN WT</strong> by 10, if you pass 3                                   arguments to print.  If you use string concatenation, you will have                               to add to spaces in the appropriate positions.




<ul>

 <li>Verify that your documentation makes sense and that you’ve added documentation to each of your functions.</li>

</ul>




<ul>

 <li><strong>Verify that your program works</strong></li>

</ul>




<ul>

 <li>Upload your file to the Program 9 dropbox folder on D2L</li>

</ul>




<strong>2.0)  EMOTICONS (60 POINTS) </strong>

<strong> </strong>

<h1>2.1)  DETAILS</h1>

<strong> </strong>

Download the plain text file “twitter_emoticons.dat”.




The file contains actual Twitter data about tweets that contained emoticons. Each row in the file represents a single tweet. Each row contains the emoticon text characters, a tweet ID, a user ID, and a timestamp.







Here are the first few lines of the file:




“D:” 5646373703 “0049961833” 20091112110207

“;-)” 5646377600 “0003829631” 20091112110222

“;-)” 5646425002 “0035714667” 20091112110544

“:(” 5646427235 “0031244602” 20091112110554 …

<strong> </strong>

The first record is from a tweet containing D: with tweet ID 5646373703, tweeted by user 0049961833 with a timestamp of 20091112110207. The second record is from a tweet containing &#x1f609; with tweet ID 5646377600, tweeted by user 0003829631 with a timestamp of 20091112110222.




For this program we’ll only be interested in the emoticon and the user ID. Create a new file called “emoticons.py”. In the file:




<ul>

 <li>Write a function called <strong>load_twitter_dicts_from_file</strong> that takes three parameters: filename (the name of a twitter data file to read), emoticons_to_ids (an empty dictionary), and ids_to_emoticons (an empty dictionary).</li>

</ul>




<ul>

 <li>The function should read the given file and load the two dictionaries with key- value pairs.  <strong>Quotes will hang the test program.  You must get rid of them.</strong>

  <ul>

   <li>emoticons_to_ids will contain the emoticons as keys. Each emoticon will have as its value a list containing the user IDs (<strong>strings – casting to </strong><strong>int</strong><strong> will hang the test</strong>) from all tweets involving that emoticon.</li>

  </ul></li>

</ul>

<strong>–</strong>there will be multiple entries in the list for users who tweeted the same emoticon on multiple occasions

<ul>

 <li>ids_to_emoticons will contain the user ID’s as keys. Each user ID will have as its value a list containing the emoticons from all tweets authored by that user. <strong>–</strong> there will be multiple entries in the list for emoticons that were used on multiple occasions</li>

 <li>NOTE: in the “.dat” file the emoticons and the user IDs are wrapped in double quotes (e.g. “;-)”. You should remove the wrapping double quotes from around emoticons and ID’s before using them as keys and values in your dictionaries.</li>

</ul>




<ul>

 <li>The function does NOT return anything.</li>

</ul>

<ul>

 <li>Write a function called <strong>find_most_common</strong> that takes a single dictionary parameter. Assume the keys of the dictionary will be strings (e.g. emoticons) and each value will be a list of strings (e.g. user ID’s).</li>

</ul>




<ul>

 <li>The function should find the key that has the longest list as a value and print    out that key and the length of its list.  Print in the following format:</li>

</ul>




<h2>&#x1f642; occurs 871 times</h2>




<u>NOTE:</u> In order to get this format you must left justify the emoticon by 21 and            then right justify the number by 9 if using string concatenation, one less in     each case if passing multiple arguments to print.  ‘occurs’ doesn’t

need to be justified.




ii.)  The function returns the key that had the longest list.




3.) In <strong>main</strong>:




<ul>

 <li>Create two empty dictionaries (emoticons_to_ids and ids_to_emoticons)</li>

</ul>




<ul>

 <li>Call your <strong>load_twitter_dicts_from_file</strong> function passing it the file name and the two dictionaries.</li>

</ul>




<ul>

 <li>Print the number of different emoticons found in the data file:</li>

</ul>




Emoticons: 98

<h2>(one space after colon)</h2>




iv.)  Print the number of different user ID’s found in the data file:




UserIDs:   2878

<h2>(three spaces after colon)</h2>







v.) Next call your <strong>find_most_common</strong>, passing it the emoticons_to_ids  dictionary.  The result should look like this:




<h3>&#x1f642; occurs 871 times</h3>




<ul>

 <li>Now pop the most common emoticon from the dictionary and again call your <strong>find_most_common</strong> function on the emoticons_to_ids Since the &#x1f642; is gone a different emoticon will be the most common.</li>

 <li>Repeat this process five times. Your output from all five function calls should look like this:</li>

</ul>




<table width="398">

 <tbody>

  <tr>

   <td width="189">            &#x1f642;</td>

   <td width="94">occurs</td>

   <td width="115">871 times</td>

  </tr>

  <tr>

   <td width="189">            &#x1f600;</td>

   <td width="94">occurs</td>

   <td width="115">377 times</td>

  </tr>

  <tr>

   <td width="189">            &#x1f641;</td>

   <td width="94">occurs</td>

   <td width="115">231 times</td>

  </tr>

  <tr>

   <td width="189">            &#x1f609;</td>

   <td width="94">occurs</td>

   <td width="115">219 times</td>

  </tr>

  <tr>

   <td width="189">            &#x1f61b;</td>

   <td width="94">occurs</td>

   <td width="115">134 times</td>

  </tr>

 </tbody>

</table>




<ul>

 <li>Verify that your documentation makes sense and that you’ve added documentation to each of your functions.</li>

</ul>




<ul>

 <li><strong>Verify that your program works</strong></li>

</ul>




<ul>

 <li>Upload your file to the Program 9 Assignments folder on D2L</li>

</ul>