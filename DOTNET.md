###### **DOTNET**

###### **(use assembly word instead of application)**

C# is a object oriented programming

Dotnet -> It is a name of initiative by Microsoft to solve the difficulties of the n tier application development - 1998



with visual basic , c++, c it is difficult in building



in n tier application there will be more business logics



application consists of

* ui/client/project logic
* business logic/process
* data logic/output



Platform dependency is the problem of n tier





**Codename -> project name**





Microsoft developed a software

* **.net framework** -> size 1 GB --> version(1.1 to 4.8(2019))
* **.net languages** -> follows CLS, CTS -> Vb.net(modified version of visual basic), C#.net, F# ------ 50+ languages are present now



\-> c# source code -> compilation -> msil(machine code) + metadata -> Assembly will be created at the end of the program



\-> assembly will be runned in the client machine



\-> in assembly(msil + metadata) - due to that it is platform independent



to run assembly - runtime is required



runtime will be installed based on the machine as it is not present in the assembly - which will be



* **.net Runtime(Common language runtime)** -> 1st only windows runtime then many other, Dotnet core framework + dotnet core runtime(2015 -free of cost for all operating systems
* 

in 2019 - .net core framework )



mono(runtime developed by other company)

restapi -> 2014-26 - simple to use with node js, express js, mongoose,



dotnet restapi built and it is 2300 times better than node js rest api





Currently

c# language - 14

sdk 10 dotnet



now

uses c# langauge - 12 and sdk 8



**Language interoperability -** any .net languages libraries can be imported and used in the class



Common language specification/common type specification - as it generated the same msil code when different languages are used and one runtime is enough to run the assembly





**assembly** -> deployable code





SingleFileAssembly ->



MultiFileAssembly ->



StrongNamedAssembly ->



GlobalAssemblyCache ->







##### **C#**



Solution folder -> project folder





One solution folder can have multiple project folder











struct

&#x20;

\- implements objects

\- encapsulation

\- inheritance cannot be done

\- all structs will be child of objects implicitly

\- can be inherited using interfaces

\- not need to write new when object instance is created



class



* \-







when we use struct over class ?

performance of struct will be more than the class









**Arrays**



collection of variables of same datatypes - homogenous

collection of variables of different datatypes - heterogenous





**Single dimensional Array:**



Syntax:

datatype\[] <arrName> = new <datatype>\[size]; --->1D



ex:

1. byte\[] marks = new byte\[10];
marks\[0] = 10;

&#x20;  marks\[10] = 99;

&#x20;  for(int i=0;i<marks.Length;i++



2\. byte\[] marks = \[10];//from .net8

&#x20;  student s = new;//from .net8

&#x20;  marks\[8] = 8;



3\. byte\[] marks = {3, 4, 6};//initializer

&#x20;  arrays can be initialized at the time of declaration of array

&#x20;  forEach(byte b in marks){WriteLine(b);}





**Multi dimensional Array:(rectangular, jagged)**



1. **Rectangular Syntax:**

&#x09;datatype\[,] arrname = new datatype\[,];



&#x09;ex:

&#x09;int\[,] cnt = new int\[5,5];

&#x09;cnt\[0,0] = 0;



&#x09;int\[]\[] cnt =

&#x20;       {

&#x20;           {1, 2, 3, 4},

&#x20;           {5, 56 2, 2},

&#x20;       };

&#x09;forEach(int b in cnt){WriteLine(b);}

&#x09;//one forEach is enough for rectangular array



**2. Jagged Syntax:**

&#x09;datatype\[]\[]\[] arrname = new datatype\[size]\[]\[];



&#x09;ex:

&#x09;int\[]\[] cnts = new int\[5]\[];

&#x09;cnt\[0] = new int\[5];

&#x09;cnt\[1] = new int\[9];

&#x09;cnt\[0]\[1] = 90;



&#x09;created by reference variables

&#x09;int\[]\[] cnt =

&#x20;       {

&#x20;           new int\[] {1, 2, 3, 4},

&#x20;           new int\[] {5, 56 2, 2, 3 24},

&#x20;       };



strings, stringbuilder - reference type for class in the type of tradition

a.





























create an interface and declare the future referencing

abstract class - instance can't created but references can be created







Top\_Down approach - interfaces

generic types(class, record, struct)

collections-

Buttom\_Up approach



Interface

Delegate



declare the delegate type

instantiate delegate variable

store address of function

use delegate to call the function











Public int ValidatePhNumber(string phoneNumber){

&#x20;   if(phoneNumber.Length != 10 || string.IsNullOrEmpty(phoneNumber))

&#x20;       rteurn -1;

&#x20;       foreach (char n in phoneNumber)

&#x20;       {

&#x20;           if(!char.IsDigit(n) || n.Equals('-'))

&#x20;           return 1;

&#x20;       }

&#x20;       return 1;

}







the code where it is executable is called native code

just  in time(JIT) - just in l(JIL)





when native aot publish is on then the code will be converted to native





interface is a pure abstract class with only declarations but in c# there will be body to the function - interface default method



Multi threaded programing

thread - is process in execution
process implemented using function
cpu will perform one function at a time
but using multithreaded the multi functions will be implemented



ex: VLC media



audio data, video data -> playaudio(), showvideo()
main(){
showvideo(); - time sharing mechanism - 1nano sec
playaudio(); - 1 nano sec

//requires parallel processing
}



80486 ht - intel processor - mmx technology - before only text and number
80586 - Pentium name



**Steps to implement Multithreading:**



communicate with runtime

system.threading

thread - abstract to interact with cpu

threadstart





1. create an object of thread class
2. pass the function you want to execute parallelly
3. start the thread
4. 



System.Threading;

void main(){

Thread video = new thread(showvideo);

Thread audio = new thread(playaudio);

video.start();

audio.start();

}

void showvideo(){}

void playaudio(){}





in this three functions are in process - main, video, audio

all the functions are completed execution then -thread is dead

how much time is allocated to the thread will be decided by cpu



garbagecollection will also performs



using round robin mechanism





threads are heavy weighted and they will directly interact with os, kernel





task - it is a high levl abstraction over thread class uses concept of threadpool

