# File Management

আমরা ফাইল নিয়ে কাজ করার সময় মুলত এই অপারেশনগুলোই করি।

- ফাইল ওপেন (File Open),
- ফাইল রিড (File Read),
- ফাইল রাইট (File Write),
- ফাইল ক্লোজ (File Close)

## ফাইল ওপেন (File Open)

```c
#include <stdio.h>

int main()
{
    FILE *fp; // Declearing File handle
    char filename[] = "my_file.txt";
    fp = fopen(filename, "w");  // Opening File With Write mode

    fprintf(fp, "This is a file created by my program!");
    fprintf(fp, "I am so happy.");

    fclose(fp);
}
```

ফাইল মোড (mode) টেবিল:

| মোড  | বর্ণনা                                                        |
| :--: | :----------------------------------------------------------- |
| `w`  | ফাইলে লেখার উদ্দেশ্য একটি ফাইল খোলা। যদি ফাইলটি না থাকে, তাহলে সেটি তৈরি করে নেয়।য় |
| `r`  | ফাইল পড়ার জন্য খোলা। অবশ্যই ফাইলটি কম্পিউটারে থাকতে হবে।        |
| `a`  | Append শব্দটি মনে রাখতে হবে। এর অর্থ হচ্ছে যোগ করা বা যুক্ত করা। এই মোডে ফাইল খোলার অর্থ হচ্ছে ফাইলটি খোলার আগে যা আছে, তা থাকবে আর সেগুলোর পর থেকে ফাইলে লেখা শুরু হবে। ফাইল না থাকলে তৈরি করে নিবে। |
| `w+` | লেখা ও পডা। তবে এটি ব্যবহার করার সময় সতর্ক থাকতে হবে। ফাইলে কোনো কিছু থাকলে সেগুলো মুছে যেতে পারে। |
| `r+` | পড়া ও লেখা                                                   |
| `a+` | ‌লেখা ও পড়া। ফাইল পড়া শুরু হবে প্রথম থেকে তবে লেখার সময় শেষ থেকে লেখা শুরু, আগের কোনো কিছু মুছবে না। |

```c
ফাংশন fopen()

প্রোটোটাইপ:
File *fopen (const char *restrict filename, const char *restrict mode);

ইনপুট:
const char *restrict filename: একটি স্ট্রিং যা ফাইলের নাম নির্দেশ করে
const char *restrict mode: একটি স্ট্রিং যা মোড নির্দেশ করে

রিটার্ন ভ্যালু:
FILE *:ফাইল পয়েন্টার বা ফাইল হ্যান্ডেল রিটার্ন করে
কোনো Error ঘোটলে NUL Pointer রিটার্ন করে

কাজ:
এই ফাংশনটি একটি ফাইল এর নাম filename ও মোড mode ইনপুট নেয় ও ফাইলটি খুলেে একটি ফাইল হ্যান্ডেল রিটার্ন করে;
```

---

## ফাইল রিড (File Read)

## 1. File Read with fscanf()

```c
#include <stdio.h>

int main()
{
    FILE *fp_in, *fp_out;
    char *input_file = "in.txt";
    char *output_file = "out.txt";
    int num1, num2, sum;

    fp_in = fopen(input_file, "r");
    fp_out = fopen(output_file, "w");

    fscanf(fp_in, "%d", &num1); // reading from file
    fscanf(fp_in, "%d", &num2); // reading from file
    
    sum = num1 + num2;
    printf("%d %d %d", num1, num2, sum);
    fprintf(fp_out, "%d\n", sum);

    fclose(fp_in);
    fclose(fp_out);

    return 0;
}
```
```c
ফাংশন fprintf()

প্রোটোটাইপ:
int fscanf(FILE  *stream, const char  *format, .... );
    
ইনপুট:
FILE *stream : একটি ফাইল হ্যান্ডেল
const char *format : একটি ফরম্যাটেড স্ট্রিং
... : ফরম্যাট স্ট্রিংয়ে অবস্হিত যতটি ফরম্যাট স্পেসিফায়ার আছে, ততটি ইনপুট

রিটার্ন ভ্যালু:
int : ঠিক কতটি ইনপুট পড়া হলো, সেই সংখ্যাটি রিটার্ন করে
কোনো Error ঘোটলে negative number  রিটার্ন করে।
    
কাজ:
এই ফাংশনটি stream ফাইল হ্যান্ডেলকে ইনপুট স্ট্রিম হিসাবে বিবেচনা করে, format স্ট্রিংয়ে নির্দেশিত ফরম্যাটে scanf ফাংশনের মতো ফরম্যাট স্পেসিফায়ারগুলোকে পরবর্তী ভ্যারিয়েবলের মান দিয়ে প্রতিস্হাপন করে ফাইলে ডেটা সংক্ষণ করে এবং কতটি ভ্যারিয়েরল ইনপুট নেওয়া হলো সেই সংখ্যাটি রিটার্ন করে।
```

## 2. File Read with fgets()

```c
#include <stdio.h>

int main() {
    FILE *fp_in;
    char *input_file = "in.txt";

    char line[80];
    
    fp_in = fopen(input_file, "r");
    
    fgets(line, 80, fp_in);
    printf("Line: %s\n", line);

    fclose(fp_in);
    return 0;
}
```
```c
ফাংশন fgets()

প্রোটোটাইপ:
char *fgets(char *str, int num, FILE *stream );
    
ইনপুট:
char *str : ইনপুট স্ট্রিম থেকে ডেটা পড়ে যেই স্ট্রিংয়ে রাখা হবে তার পয়েন্টার
int num: সর্বমোট কয়টি ক্যারেক্টার পড়া হবে
FILE *stream : যেই ফাইল থেকে ডেটা পড়া হবে তার হ্যান্ডেল

রিটার্ন ভ্যালু:
char * : ঠিকঠাক মতো পড়া শেষ হলে যেই স্ট্রিংয়ে ডেটা রাখা হলো তার পয়েন্টার রিটার্ন করে। এছাড়া কোন কারণে ডেটা পড়া না গেলে NULL পয়েন্টার রিটার্ন করে।
    
কাজ:
stream ফাইল হ্যান্ডেলকে ইনপুট স্ট্রিম হিসাবে বিবেচনা করে, num-1 সংখ্যক ক্যারেক্টার পড়বে। num-1 সংখ্যক ক্যারেক্টার পড়ার আগেই EOF বা নিউলাইন পেয়ে গেলে পড়া বন্ধ করবে ও str রিটার্ন করে। ফাইল পড়তে কোনো error হলে NULL পয়েন্টার রিটার্ন করে।
```

## ফাইল রাইট (File Write)

```c
#include <stdio.h>

int main()
{
    FILE *fp;

    char filename[] = "my_file.txt";

    fp = fopen(filename, "w");

    fprintf(fp, "This is a file created by my program!");  // writing into file
    fprintf(fp, "I am so happy.");  // writing into file

    fclose(fp);
}
```

```c
ফাংশন fprintf()

প্রোটোটাইপ:
int fprintf(FILE  *stream, const char  *format, .... );
    
ইনপুট:
FILE *stream : একটি ফাইল হ্যান্ডেল
const char *format : একটি ফরম্যাটেড স্ট্রিং
... : ফরম্যাট স্ট্রিংয়ে অবস্হিত যতটি ফরম্যাট স্পেসিফায়ার আছে, ততটি ইনপুট

রিটার্ন ভ্যালু:
int : ঠিক কতটি ক্যারেক্টার লিখা হলো, সেই সংখ্যাটি রিটার্ন করে
কোনো Error ঘোটলে negative number  রিটার্ন করে
    
কাজ:
এই ফাংশনটি stream ফাইল হ্যান্ডেলকে আউটপুট স্ট্রিম হিসাবে বিবেচনা করে, format স্ট্রিংয়ে নির্দেশিত ফরম্যাটে printf ফাংশনের মতো ফরম্যাট স্পেসিফায়ারগুলোকে পরবর্তী ভ্যারিয়েবলের মান দিয়ে প্রতিস্হাপন করে ফাইলে ডেটা রাইট করে এবং কতটি ক্যারেক্টার রাইট করা হলো, সেই সংখ্যাটি রিটার্ন করে।
```

## ফাইল ক্লোজ (File Close)

```c
#include <stdio.h>

int main()
{
    FILE *fp;

    char filename[] = "my_file.txt";

    fp = fopen(filename, "w");

    fprintf(fp, "This is a file created by my program!");
    fprintf(fp, "I am so happy.");

    fclose(fp); // closing file
}
```

```c
ফাংশন fclose()

প্রোটোটাইপ:
int fclose(FILE  *stream );
    
ইনপুট:
FILE *stream : একটি ফাইল হ্যান্ডেল

রিটার্ন ভ্যালু:
int : ফাইলটি সফলভাবে বন্ধ হলে 0 রিটার্ন করে, নাহলে EOF রিটার্ন করে
    
কাজ:
stream এ নির্দেশিড ফাইলটি রন্ধ করে।
```

