# TypeScipt


https://www.w3schools.com/typescript/exercise.php?filename=exercise_enums1
***********************************************************************

{let,var,const} {variable} :{readonly} {string,number,any,boolean,model?}  []=
***********************************************************************
tsc index --watch
TypeScript allows developers to add 
----- to JavaScript.

*types

معنى كلمة "loosely typed" في جافاسكريبت
في جافاسكريبت، تُشير كلمة "loosely typed" إلى نظام الكتابة الديناميكي الخاص بها. يعني ذلك أن نوع المتغير أو التعبير غير مُعلن صراحةً ويمكن تغييره وقت التشغيل بناءً على القيمة التي يحملها.

يُقابل ذلك اللغات "strongly typed" ، حيث يتم إعلان أنواع المتغيرات مسبقًا ويتم تطبيقها طوال البرنامج.
-------------------------------------
The TypeScript compiler can be configured with which file?

يمكن تكوين مترجم TypeScript باستخدام أي ملف؟
tsconfig
--------------------------------------------------------------------
There are two main ways TypeScript assigns a type:
?
هناك طريقتان رئيسيتان لتعيين TypeScript للنوع:

Explicit
Implicit

-------------------------------------------------------------
Create a "firstName" variable, string type using Implicit type:

let --- firstName ---= "Dylan";
--------------------------------------------------------------
Create a "firstName" variable, string type using Explicit type:

let 
------ firstName ----------
: 
---------String-------------
 = "Dylan";
----------------------------------------
Create an empty "myVar" variable, and disable type checking:
قم بإنشاء متغير "myVar" فارغًا، وقم بتعطيل التحقق من النوع:

let myVar:
----------------------------------------------------

 ----------- any -----------

disable type checking:any

 وقم بتعطيل التحقق من النوع
-------------------------------------------------------------------
Create an empty "myVar" variable, and specify it should be an unknown type:

قم بإنشاء متغير "myVar" فارغًا، وحدد أنه يجب أن يكون من النوع غير المعروف:

------------------------------------------------------------------
Create an empty "myVar" variable, and specify it should be an unknown type:

قم بإنشاء متغير "myVar" فارغًا، وحدد أنه يجب أن يكون من النوع غير المعروف:
let myVar: 
unknown
;
-----------------------------------------------------------------------
let  x :number ;
x = "hello"    خطأ

-----------------------------------
npm install -g typescript
----------------------------
بنعمل كومبايل لملفات التايب سكريبت عشان نحولهم للجافا سكريبت عشان يفهمهم الكروم

tsc {filename.ts}
-----------------------------------------------------
ts
let arr:number []; 
arr=[1,3,4,5,6];

js
var arr;
arr = [1, 3, 4, 5, 6];

------------------------------------------------------------
Prevent the array from being changed:
منع تغيير المصفوفة

readonly
--------------------------------------------------------
ts & js
const names:readonly string[]=["string","comrade"];
var names = ["string", "comrade"];
---------------------------------------------------------
هذا يسمى ب Tuples
const person: [string, number, boolean] = ['John Doe', 30, true];

السؤال الان

The order of value types does not matter for Tuples:
ترتيب الداتا تايب غير مهم في حالة ال tuples
? الجواب هو ان الترتيب مهم
---------------------------------------------
Define ourTuple as string and boolean, in that order:
let ourturple :[string,boolean];

اما الشكل في جافا سكريبت كالتالي 
var ourturple;

------------------------------------------------------------------
اعملي اراي من اي نوع بدك اياه بلتايب سكريبت
let arr:any []=[1,"str",2
25];
******************************************************************
{let,var,const} {variable} :{readonly} {string,number,any,boolean}  []=
***********************************************************************
//union   |
اتحاد    Or

tsc {tsfilename} = typeScriptCompile

let n :number | boolean | string ;
---------------------------------------------------------------------
//Enum

enum Weeks {
    sat,
    sun,
    mon,
    tues,
    wed,
    thurs,
    fri 
  }

tsc index

  
  console.log(Weeks.sat); // Access enum values using the enum name
------------------------------------------------------
js

var Weeks;
(function (Weeks) {
    Weeks[Weeks["sat"] = 0] = "sat";
    Weeks[Weeks["sun"] = 1] = "sun";
    Weeks[Weeks["mon"] = 2] = "mon";
    Weeks[Weeks["tues"] = 3] = "tues";
    Weeks[Weeks["wed"] = 4] = "wed";
    Weeks[Weeks["thurs"] = 5] = "thurs";
    Weeks[Weeks["fri"] = 6] = "fri"; // Corrected typo: 'fri' instead of 'friday'
})(Weeks || (Weeks = {}));
console.log(Weeks.sat); // Access enum values using the enum name

--------------------------
index.html

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>

/////////////////////
console,log(weeks.sat) ////output// =0
/////////////////////

    <script src="./index.js"> </script>
</head>
<body>
    
</body>
</html>

---------------------------------------
--------------------------------------------------------
Specify that the second property, called model, should be optional:

const car: { type: string, 
model?
: string } = {
  type: "Toyota"
};

---------------------------------------------------------------------------------------------------------
enum Weeks {
    sat,
    sun,
    mon,
    tues,
    wed,
    thurs,
    fri 
  }
  
  console.log(Weeks.sat); // Access enum values using the enum name

لاحظ استخدمنا اشارة المعكوفة الاقواس
زي تاعت الاوبجيكت

----------------------------
enum Weeks {
    sat=1,
    sun,
    mon,
    tues,
    wed,
    thurs,
    fri 
  }
  
  console.log(Weeks); // Access enum values using the enum name

output//{
    "1": "sat",
    "2": "sun",
    "3": "mon",
    "4": "tues",
    "5": "wed",
    "6": "thurs",
    "7": "fri",
    "sat": 1,
    "sun": 2,
    "mon": 3,
    "tues": 4,
    "wed": 5,
    "thurs": 6,
    "fri": 7
}

لاحظ ان الانديكس صار يبلش من 1 مش من 0

-------------------------------------------------
ENUM في TypeScript

ENUM (اختصار لـ Enumeration) هو نوع بيانات مُستخدم لتعريف مجموعة من القيم الثابتة المسماة في TypeScript. تُستخدم ENUMs بشكل شائع لتمثيل مجموعات محددة من الخيارات أو الحالات، مثل أيام الأسبوع أو أنواع العملات أو أحجام الملفات.

خصائص ENUMs في TypeScript:

الثبات: القيم في ENUM ثابتة، أي لا يمكن تغييرها بعد تعريفها.

المسماة: لكل قيمة في ENUM اسم فريد.

مرتبة: يتم ترتيب قيم ENUM بشكل افتراضي، مع بدء الترقيم من 0.

نوع البيانات: يمكن أن تكون قيم ENUM من أنواع بيانات مختلفة، مثل الأعداد الصحيحة أو السلاسل أو حتى أنواع بيانات مخصصة.

التوافق مع IntelliSense: توفر ENUMs تجربة IntelliSense غنية في TypeScript، مما يسهل على المطورين اكتشاف واستخدام قيم ENUM.

فوائد استخدام ENUMs في TypeScript:

تحسين قابلية القراءة: تجعل ENUMs الكود أكثر قابلية للقراءة وفهمًا من استخدام القيم العددية الخام أو السلاسل النصية.

منع الأخطاء: تساعد ENUMs في منع الأخطاء عن طريق ضمان استخدام القيم الصحيحة فقط من مجموعة محددة.

تحسين الصيانة: تجعل ENUMs الكود أكثر قابلية للصيانة، حيث يمكن تغيير معنى قيمة ENUM في مكان واحد دون الحاجة إلى تعديل الكود في جميع الأماكن التي تستخدمها.

التوافق مع أنواع البيانات الأخرى: يمكن استخدام ENUMs مع أنواع بيانات أخرى في TypeScript، مثل الكائنات والوظائف والواجهات.

مثال على استخدام ENUM في TypeScript:

TypeScript

enum WeekDays {

  Sunday = 0,

  Monday = 1,

  Tuesday = 2,

  Wednesday = 3,

  Thursday = 4,

  Friday = 5,

  Saturday = 6

}

const today: WeekDays = WeekDays.Wednesday;

console.log(today); // Output: 3 (الرقم المخصص ليوم الأربعاء)

console.log(WeekDays[3]); // Output: Wednesday (اسم يوم الأربعاء)

في هذا المثال، يتم تعريف ENUM يسمى WeekDays لتمثيل أيام الأسبوع. ثم يتم تعيين متغير today لقيمة WeekDays.Wednesday. عند طباعة today، يتم إخراج "3" (الرقم المخصص ليوم الأربعاء). عند طباعة WeekDays[3]، يتم إخراج "Wednesday" (اسم يوم الأربعاء).

ملاحظات:

يمكن تعريف ENUMs في أي مكان في ملف TypeScript، بما في ذلك داخل الكائنات والوظائف والواجهات.

يمكن أن تحتوي ENUMs على قيم مخصصة، مثل الوظائف أو الكائنات.

يمكن استخدام ENUMs مع أنواع البيانات الأخرى في TypeScript لإنشاء أنواع بيانات مخصصة قوية.

في الختام، تعد ENUMs أداة قوية وفعالة لتعريف مجموعات محددة من القيم الثابتة في TypeScript. تُستخدم بشكل شائع لتحسين قابلية القراءة والوقاية من الأخطاء وجعل الكود أكثر قابلية للصيانة، وتوفر تجربة IntelliSense غنية للمطورين.
---------------------------------------------------------
Union
---------------------------------------------------------





Function in TypeScript
-----------------------------------------------------------------------------

function {functionName} ({variable}:{dataType}){

}
---------------------------------------------------------------
//getName
function getName  (name:string) {
console.log(name);}
//or
function getNamee  (name:string) {
  console.log(name);}
  // this is false
//function getNamme  (name:string):string {
//console.log(name);}
//always console.log with (VOID)
// // // // // // // // // / // // // // // // // // // //
//Void
function sum1 (){
  console.log (2+2);
}

//Void
function sum2 () :void{
  console.log (2+2);
}

function sum3(a: number, b: number): void { 
  console.log(a + b);
}

let x=  function sum4(a: number, b: number): void { 
  console.log(a + b);
}


////////////////////////////////////////////////////////
optional in typeScript
//////////////////////////////////////////////////////////
function myFunc(myVar1:string,myVar2?:string) :string {
  return(myVar1);
  }

function myFunc(myVar1:string,myVar2:model?){
return(myVar1 + (myVar2 || ""));
}

-------------------------------------------------------------------------------------------------------------------------------------------------------

-----------------------------------------------------------------------------------------------------------------------------------------
-----------------------------------------------------------------------------------------------------------------
