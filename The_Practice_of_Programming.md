# The Practice of Programming

1. Simplicity, clarity and generality form the bedrock of good software.

2. Good code has...
  * straightforward logic
  * natural expression
  * conventional language use
  * meaningful names
  * neat formatting
  * helpful comments
  * avoid clever tricks and unusual constructs

3. Macro names should not indicate specific values. The name will also need to be changed later if the use changes.
   ```
Don't:
#define ONE 1
#define TEN 10

Do:
#define INPUT_MODE 1
#define BUFFER_SIZE 10
   ```

4. Use long descriptive names for globals, short names for local variables.
   ```
Don't:
for (ElemenIndex = 0; ElementIndex < nelems; ElementIndex++)

Do:
for (i = 0; i < nelems; i++)
   ```
   ```
Don't:
int nelms = 3; // global variable

Do:
int number_of_buffer_elements = 3; // global variable
   ```

5. Consistent adherence to a coding convention is more important than having favoring specific ones.
   ```
Don't:
int numberElements = 3;
int buffer_size = 10;

Do:
int number_elements = 3;
int buffer_size = 10;
   ```

6. Give related things related names.
   ```
Don't:
class UserQueue
{
    int noOfItemsInQ, frontOfTheQueue, queuecapacity;
    public int noOfUsersInQueue();
}

* Inconsistent use of Q, queue and Queue.
* Member variables don't need to mention 'queue' since that is implied.

Do:
class UserQueue
{
    int nitems, front, capacity;
    public int nusers();
}
   ```

7. Use active names for functions. Function names should start with a verb followed by a noun(s).
   ```
Don't:
currentTime();

Do:
getCurrentTime();
   ```

8. Function names should indicate return type if possible.
   ```
Don't:
if (checkoctal(x))

Do:
if (isoctal(x))
   ```

9. Use natural forms of expressions. Negations are always tough to understand.
   ```
Don't:
if ((!block_id < actblks) || !(block_id >= i))

Do:
if ((block_id >= actblks) || (block_id < i))
   ```
10. Avoid too many complex expressions in a single line.
   ```
   Don't:
   *x += (*xp=(2*k < (n-m) ? c[k+1]:d[k--]));

   Do:
   if (2*k < (n-m))
   {
       *xp = c[k+1];
   }
   else
   {
       *xp = d[k--];
   }
   *x += *xp
   ```

11. Align if-else statements for maximum readability.
   ```
   Don't:
   if (c1)
       if (c2)
           if (c3)
               // do stuff
           else
               print
       else
           print
   else
       print

   Do:
   if (!c1)
       print
   else if (!c2)
       print
   else if (!c3)
       print
   else
       // do stuff
   ```
   
12. Avoid function macros.
   ```
   * The avoided function call overhead is not worth the amount of problems it can create.
   * Modern compilers and processors make this optimization irrelevant.
   
   Don't:
   #define isupper(c) ((c) >= ' A ' && (c) <= 'Z')

   Problem when called as: while (isupper(c = getchar()))
   ```

13. Use const instead of macros. 
   ```
   * 'Macros are a dangerous way to program because they change the lexical structure of the program underfoot.'
   * Macros are hard to debug. You don't know exactly what they translated to and they don't necessarily correspond line-to-line with source code.
   * Macros are simple text-substitution. They are not bound by the rules of the language.

Don't:
#define ON 1
#define OFF 0

Do:
const int on = 1;
const int off = 0;
   ```
14. Comments should add something that is not obvious from the code. It should not re-state the obvious.
   ```
Don't:
count++;   // increments count

Do:
count++;   // now we point to the end of the list
   ```

15. Comment all functions and global variables.
   ```
Do:
const int total_elements = 5;
struct node
{
    int data;            // holds the data
    struct node *next;   // pointer to next node element
};
   ```

16. Don't comment bad code - rewrite it. If it takes more than a few lines to explain whats happening, you should probably rewrite it. Good code needs fewer comments than bad code.
