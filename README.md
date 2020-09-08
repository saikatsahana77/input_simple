# Input_simple

> A One-stop Python Package for all your input needs.

---

### Table of Contents

Navigate to your Preferred Section:

- [Description](#description)
- [How To Use](#how-to-use)
- [License](#license)
- [Author Info](#author-info)

---

## Description

This is a package for working with input Files in Python. This Package gets you Evrything your Require for working with input from simple task like generating a Integer Array from a Space seperated string to creating test inputs to check your program effectively.

#### Technologies/Languages Used

- Python

[Back To The Top](#Input_simple)

---

## How To Use

## Installation

### Windows:

```python3
>>> pip install input-simple
```

### Mac/Linux:

```python3
>>> sudo pip3 install input-simple
```

## Usage

```python3
>>> import input_simple
```

This will ensure that you have imported the module correctly.

### Now let's explore Different Methods:

1. seperate_list

   Usage:

   ```python3
   import input_simple
   k = input_simple.seperate_list("Saikat Sahana 1 2  2.56")
   print(k)
   ```

   This takes the string and seperates it on the points where spaces are provided. It auto detects if a value is string or float or int and the output list that you get for that reflects that by converting it to the suitable datatype. You can also change the delimeter from "&nbsp; " to some other for that, you have to pass a extra delimeter.

   ```python3
   import input_simple
   k = input_simple.seperate_list("Saikat Sahana 1 2  2.56",":")
   print(k)
   ```

   Now the string splits at those points where it finds a ":".

2. seperate_list_int

   Usage:

   ```python3
   import input_simple
   k = input_simple.seperate_list_int("12 15 22 2.56")
   print(k)
   ```

   This takes a string similar to the previous method but returns a integer array no matter whatever the datatype maybe. However this method will throw a eroor if you pass string values in the seperated elements as they cannot be converted to integer. Also this method has the extra optional parameter of the delimeter that seperates the string which is set to "&nbsp; " by default.

3. seperate_list_str

   Usage:

   ```python3
   import input_simple
   k = input_simple.seperate_list_int("Saikat Sahana 12 22 2.56")
   print(k)
   ```

   This takes a string similar to the previous method but returns a string array no matter whatever the datatype maybe. Also this method has the extra optional parameter of the delimeter that seperates the string which is set to "&nbsp; " by default.

4. text_to_inp

   Usage:

   ```python3
   import input_simple
   k = input_simple.text_to_inp("input.txt")
   print(k)
   ```

   This method takes a text file(here we suppose the name of the text file as input, use your preffered name) and fetches its data of each line,converts it into a test case, and then goes through each line and breaks them into elements when it encounters "&nbsp; &nbsp; " as a delimeter for different elements and taking "&nbsp; " for seperating a string to array. In case your file contains a string element which contains more than one word then you are prompted in terminal that if you want to consider it as a string type "str"(without the qoutes) and for considering it as a array type "str-arr" (without qoutes). Also this method has two optional extra parameters, first one is the delimeter by which the elements are separated and second one by which the array is seperated if present.

   ```python3
   import input_simple
   k = input_simple.text_to_inp("input.txt",":",",")
   print(k)
   ```

   Here the values would be separated on ":" and the if array is present it's elements would be seperated by ",".

5. csv_to_inp

   Usage:

   ```python3
   import input_simple
   k = input_simple.csv_to_inp("input.csv")
   print(k)
   ```

   CSV is comma seperated values file where each element is generally seperated by comma (in some cases by other delimeters too). This method takes a csv file(here we suppose the name of the text file as input, use your preffered name) and fetches its data of each line,converts it into a test case, and then goes through each line and breaks them into elements when it encounters "," as a delimeter for different elements and taking "&nbsp; " for seperating a string to array. In case your file contains a string element which contains more than one word then you are prompted in terminal that if you want to consider it as a string type "str"(without the qoutes) and for considering it as a array type "str-arr" (without qoutes). This method also has two optional parameters for replacing the "," and "&nbsp; " with something else.

6. xls_to_inp

   Usage:

   ```python3
   import input_simple
   k = input_simple.xls_to_inp("input.xlsx")
   print(k)
   ```

   This method takes a xlsx file(here we suppose the name of the text file as input, use your preffered name) and fetches its data of each line,converts it into a test case, and then goes through each line and breaks them into elements when it encounters a cell in excel as a delimeter for different elements and taking "&nbsp; " for seperating a string to array. In case your file contains a string element which contains more than one word then you are prompted in terminal that if you want to consider it as a string type "str"(without the qoutes) and for considering it as a array type "str-arr" (without qoutes). it also has a optional parameter that replaces the "&nbsp; " delimeter to some other value for separating elements in an array.

   ```python3
   import input_simple
   k = input_simple.xls_to_inp("input.xlsx",":")
   print(k)
   ```

   This will seperate elements inside array from string to array based on where they encounter a ":".

7. dummy_inp

   Usage:

   ```python3
   import input_simple
   k= input_simple.dummy_inp([['int',10,20],['str','[A-Za-z]{5}[0-9]{4}']])
   print(k)
   ```

   This method creates a dummy input each time you call this method. This Method can be used for testing you program under different test cases for competetive coding. The format of using this method is using passing a [], inside which you make more [] and each of them corresponds to one element and their info. Different Values that can be passed are:

   - int - Format - ['int', lower_bound, upper_bound]
   - float - Format - ['float', round_off_value, lower_bound, upper_bound]
   - string - Format - ['str', regular_expression in qoutes]
   - int-arr - Format - ['int-arr', no_of_elements, lower_bound, upper_bound]
   - float-arr - Format - ['float-arr', no_of_elements, round_off_value, lower_bound, upper_bound]
   - string-arr - Format - ['str-arr', no_of_elements, regular_expression in qoutes]

[Back To The Top](#Input_simple)

---

## License

MIT License

Copyright (c) [2020] [Saikat Sahana]

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.

[Back To The Top](#Input_simple)

---

## Author Info

- Youtube - [Tech Rack](https://www.youtube.com/TechRack)
- Twitter - [@sahana_saikat](https://twitter.com/sahana_saikat)
- Website - [Tech Rack](https://tech-rack.in)
- Facebook - [Saikat Sahana](https://www.facebook.com/saikat.sahana.75)
- Instagram - [saikat2811](https://www.instagram.com/saikat2811/)
- LinkedIn - [Saikat Sahana](https://www.linkedin.com/in/saikat-sahana-454608118)
- Github - [saikatsahana77](https://github.com/saikatsahana77)

[Back To The Top](#Input_simple)
