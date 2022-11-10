
  # 15 C# best/secure coding practices</h1>

  ### 1. Avoid the use of underscore while naming identifiers
        
  ```c#
   ///<summary>corrrect practice</summary>
        public String firstName;

        ///<summary>wrong pracice</summary>
        public String first_Name;
  ```

### 2. Naming convention
  **Pascal Convention:First character of all words should be in uppercase and others in 
      lowercase.Use pascal
        casing for naming classes,records, or structs.For interface,prefix the name with an "I".For public members of types,such as fields,properties
        ,events,methods, and local functions,use pascal casing too**

  ```c#
    ///<summary>correct practice</summary>
        public record UserInfo
        (
            string firstName,
            string lastName,
            string phoneNumber
        );
        public struct RoadMap
        {
        }
        public interface IClasslList
        {

        }
        public class TotalTasks
        {
            public bool IsFalse;
            public ITaskQueue TaskQueue { get; init; }
            public event Action TaskSubmission;

        public void StartTaskSubmission()
        {
                static int CountTotalTasks() => TaskQueue.Count;
        }
            }


        ///<summary>
        /// wrong practice
        /// </summary>
        public record userInfo
        (
            string firstName,
            string lastName,
            string phoneNumber
        );
        public struct roadMap
        {
        }
        public interface iclasslList
        {

        }
        public class totalTasks
        {
            public bool isFalse;
            public iTaskQueue TaskQueue { get; init; }
            public event Action taskSubmission;

            public void startTaskSubmission()
            {
                static int countTotalTasks() => taskQueue.Count;
            }
        }
  ````

  ### 3. Avoid the use of system type names
  ```c#
        ///<summary>correct practice</summary>
        string address;
        int numbers;
        bool isTrue;
        ///<summary>wrong practice</summary>
        String address;
        Int32 numbers;
        Boolean isTrue;
  ```

  ### 4. Camel Case Convention

  **The first character of all words of every local variable,
        except the first word,is upper case and other characters are lowercase.**
        
  ```c#
  ///<summary>correct practice</summary>
        int evenNumbers;
        string fullName;

        ///<summary>wrong practice</summary>
        int evennumbers;
        string fullname;
  ```

### 5. Constants should always be declared in UPPER_CASE      
  ```c#
  ///<summary>[.]Correct practice</summary>
        public const string USERNAME = "Chizoba";

        ///[]<summary>Bad practice</summary>
        public const string username = "Chizoba";
  ```

### 6. Placement of comments

  **Place comments on separate lines,not at the end of the lines of codes,begin comments
        with uppercase and end it with a period**
        
  ```c#
  ///<summary>good practice</summary>
        string footWare = "sneakers";

        // The is a correct commment format.
        //[]/<summary>bad practice</summary>
        string footWare = "sneakers"; // the is a correct commment
  ```

### 7. Alignment of curly braces

  **For better code indentation and readability,always align the curly braces vertcally**
        
  ```c#
        ///<summary>correct practice</summary>
        class CurlyBraces
        {
            static void ShowBraces()
            {

            }
        }


        ///<summary>wrong  practice</summary>
        class CurlyBraces
        {
            static void ShowBraces()
            {

               }
           }
  ````

### 8. Naming of Variables

  **Use meaningful and descriptive words to name variables, avoid abbreviations**
        
  ```c#
      ///<summary>correct practice</summary>
        string[] cars = { "Benz", "Ford", "volvo" };
        string userName = "Alice";
        ///<summary>wrong practice</summary>
        string[] cars = { "fork", "plate", "pot" };
        string uName = "Alice";
  ```

### 9. Method name should be meaningful
  ```c#
**Method name should be meaningful**
///<summary>Good practice</summary>
private void UserInfo(string firstName, int age);
///<summary>Bad practice</summary>
private void FoodRecipe(string firstName, int age);
  ```

  ### 10. Do declare all member variables at the top of a class, with static variables at the very top.
  ```c#
  ///<summary>Good praactice</summary>
public class Trainee
{
Public string traineeName{get;set;};
Public int traineeGroup{get;set};
Public Trainee()
{
//..
}
}
 ///<summary>Bad practice</summary>
 public class Trainee
{
Public string traineeeName{get;set;};
Public int traineeGroup{get;set};
Public Trainee()
{
//..
}
}
  ```
### 11. Do not suffix enum names with Enum.

  ```c#
  ///<summary>good practice</summary>
Public  DirectionEnum
{
//..
}
 ///<summary>bad practice</summary>
Public enum DirectionEnum
{
//..
}
  ```
  ### 12. Always use braces ({}) for single conditional if statement, for and foreach loops
  **Without the braces, it is too easy to accidentally add a second line thinking it is included in the if, when it isn’t.**

  ```c#
  ///<summary> Bad practice</summary>
if(conditioin) action;

 ///<summary>Good practice</summary>
if (condition) 
{ 
    action; 
}

  ```
  #### 13. Avoid the use multiple if-else statements, use switch case instead
  ```c#
  ///<summary> Good practice</summary>

switch(condition)
{
   case 1:
      //do something
      break;
   case 2:
      //do something
      break;
   case 3:
      //do something
      break;
   default:
      //do something else
     break;
}
  ///<summary>bad practice</summary>
if (condition)
{
   //do something
}
else if(condition)
{
   //do something
}
else if(condition)
{
   //do something
}
else(condition)
{
   //do something else
}

  ```
  ### 14. Use object and collection initializers when initializing objects:
```c#
///<summary>Bad Practice</summary>
Person person = new Person();
person.FirstName = "Vianne";
person.LastName = "Durano";

///<summary>Good Practice</summary>
var person = new Person { 
	FirstName = "Vianne",
	LastName = "Durano"
};

  ```
### 15.Use nouns or adjective phrases for Property names. 
  **When naming boolean properties or variables, you may add the prefix "can", "is", "has", etc.**
  ```c#
  ///<summary>Good Practice</summary>
public bool IsActive { get; set; }
public bool CanDelete { get; set; }

//variables
bool hasActiveSessions = false;
bool doesItemExist = true;
///<summary>Bad Practice</summary>
public bool Active { get; set; }
public bool Delete { get; set; }

//variables
bool ActiveSessions = false;
bool ItemExist = true;
  ```
