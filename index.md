#include <cstdlib>
#include <iostream>
#include <iomanip>
#include <fstream>
#include <string>
#include <vector>
using namespace std;
  
void loadVectorsFromFile(); //loads lists from grocery.txt
void saveVectorsToFile(); //saves lists to grocery.txt
void recipesEditor();//display's edit the list menu
void menu();
void recipeInsert();
void recipeEditor();
void recipeDatabase();

int mainChoice;
int choice;
string str;
const int runningInt = 1;

int recipesChoice;
vector<string> recipesList;
int recipesSize;

void saveVectorsToFile(){
    ofstream recipesOut("recipe.txt");
    for (int x = 0; x < recipesSize; x++){
           recipesOut << recipesList[x] << endl;
           }
           recipesOut.close();
    }

void menu(){
  cout << "\nWelcome to the Recipe Menu Selector.\n \nPlease choose what you would like to do!\n\n";
  cout << "1. Insert New Recipe Ingredients.\n";
  cout << "2. Edit Current Recipe Ingredients.\n";
  cout << "3. Save and Exit the Database.\n";
  cout << "Your Choice: "; 
  }

fstream recipesFile ("recipe.txt");//ANDREW:I created the empty file for you
 //display's main menu (i consider the 1st menu main)
//declare void exit here


int main(){
  while(runningInt == 1){
  menu();

  cin >> choice;
  switch(choice){ //case used for main menu switch
  case 1:  recipeInsert();
    break; //Insert Recipe 
  case 2:  recipeEditor();
    break; //edit and save
  case 3: 
    cout << "Saving and Exiting Database!";
    saveVectorsToFile();
    exit(0);
  default:
    break;//exit switch to exit program
    }
  }
}



void loadVectorsFromFile(){
  while(getline(recipesFile, str)){
    if(str.size() > 0){
      recipesList.push_back(str);
    }
  }
}
void recipeInsert(){
  recipesChoice = 0;
    if(recipesChoice == 1||2||3 )
      cout <<"\nYour current Recipe Database is:\n\n";
       for (int x = 0; x < recipesSize; x++){
            cout << x + 1 << ". " << recipesList[x] << endl;
      # include "loopy.h" 
      }
}
       cout << "\nWhat would you like to add to this list: ";
        cin >> recipesChoice;
        switch(recipesChoice){
            case 1: {
                string recipesAddition;
                cin.ignore();
                getline(cin, recipesAddition);
                recipesList.push_back(recipesAddition);
                recipesSize++;
                cout << "\n" << recipesAddition << " has been added to the list!" << "\n";                
                break;
            }
            case 2:
                int recipesRemoval;
                cout << "\nPlease enter which item you would like to remove: ";
                cin >> recipesRemoval;
                recipesList.erase(recipesList.begin() + recipesRemoval - 1);
                recipesSize--;
                break;
              break;
            default: 
               break; 
        }
    }




void recipeEditor(){
}
    
              


/* ******ORIGINAL*DO*NOT*EDIT*******   
   cout << "\nWhat would you like to do?\n\n1. Add to this list\n2. Remove from this list\n3. Return to the main menu\n\nPlease select: ";
        cin >> recipesChoice;
        switch(recipesChoice){
            case 1: {
                string recipesAddition;
                cout << "Please enter what you would like to add to the list: ";
                cin.ignore();
                getline(cin, recipesAddition);
                recipesList.push_back(recipesAddition);
                recipesSize++;
                cout << recipesAddition << " has been added to the list!";                
                break;
            }
            case 2:
                int recipesRemoval;
                cout << "Please enter the number of which item you would like to remove: ";
                cin >> recipesRemoval;
               recipesList.erase(recipesList.begin() + recipesRemoval - 1);
                recipesSize--;
                break;
                
  void saveVectorsToFile()
    {
    ofstream recipesOut("grocery.txt");
    for (int x = 0; x < recipesSize; x++){
           recipesOut << recipesList[x] << endl;
           }
           recipesOut.close()
        }
  }
}*/
