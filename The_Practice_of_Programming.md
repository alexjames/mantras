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
