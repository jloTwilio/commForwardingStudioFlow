# commForwardingStudioFlow
This studio flow will forward calls and messages to defined cell number.  Calling in to this number from the defined cell will allow messages or calls to be sent back to last caller, or send-to can be defined.

To set up - 
  1. Create a new Standard API Key for account you'd like to use.  Save Key & Secret.
  2. create new Studio Flow.  Choose to create from JSON.  Paste in contents of JSON file here.
  3. open new Flow.  Click on "set_EnvironmentVariables" widget. For each of first 3 variables, click edit and change to:
     a. yourCellNumber - your home cell you'd like to forward calls and messages to
     b. API_key - API key created in step 1
     c. API_secret - API Key Secret created in step 1
  4. Save and Publish
  5. Go to Active Numbers.  Click on the number you'd like to use as your Mask number.  For both Voice and Messaging, choose your new Studio Flow.

To use - 
Messaging:
All inbound messages will be sent to you from your Masking Phone Number.  They will begin with the number the message was sent from orginally.  
If you reply with a basic message, the system will find the last inbound SMS and ask if you'd like to send your message to that number.  You can accept or ask to find an older number.  There is a limit of 15 loop attempts, so how many older numbers you can access will vary. 
At any time, you can reply with "+1xxxxxxxxxx/~Your message body".  This will send the message after "/~" to the number listed before.  

Calling:
Calls will be shown in your phone as coming from the original caller.  You can call them directly back on that number, but this will be shown from your personal cell.  
Calls from your cell into the Masked Number will offer you the chance to use the keypad to enter the desired number or to look up the last inbound caller.  You can accept the number found or find an older number.  There is a limit of 15 loop attempts, so how many older numbers you can access will vary. 
 
