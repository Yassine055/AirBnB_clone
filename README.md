# 0x00. AirBnB clone - The console

## 0x00.Table of contents

* [0x01 Introduction](#0x01-Introduction)
* [0x02 Environment](#0x02-Environment)
* [0x03 Installation](#0x03-Installation)
* [0x04 Testing](#0x04-Testing)
* [0x05 Usage](#0x05-Usage)
* [0x06 Authors](#0x06-Authors)

## 0x01 Introduction

Team project to build a clone of [AirBnB](https://www.airbnb.com/).

The console is a command interpreter to manage objects abstraction between objects and how they are stored.

The console will perform the following tasks:

* create a new object
* retrive an object from a file
* do operations on objects
* destroy an object

## Storage :baggage_claim:

The above classes are handled by the abstracted storage engine defined in the 
[FileStorage](./models/engine/file_storage.py) class.

Every time the backend is initialized, AirBnB_clone instantiates an instance of 
`FileStorage` called `storage`. The `storage` object is loaded/re-loaded from 
any class instances stored in the JSON file `file.json`. As class instances are 
created, updated, or deleted, the `storage` object is used to register 
corresponding changes in the `file.json`.

## Console :computer:

The console is a command line interpreter that permits management of the backend 
of HolbertonBnB. It can be used to handle and manipulate all classes utilized by 
the application (achieved by calls on the `storage` object defined above).

### Using the Console

The AirBnB_clone console can be run both interactively and non-interactively. 
To run the console in non-interactive mode, pipe any command(s) into an execution 
of the file `console.py` at the command line.


## 0x02 Environment

<!-- ubuntu -->
<a href="https://ubuntu.com/" target="_blank"> <img height="" src="https://img.shields.io/static/v1?label=&message=Ubuntu&color=E95420&logo=Ubuntu&logoColor=E95420&labelColor=2F333A" alt="Suite CRM"></a> <!-- bash --> <a href="https://www.gnu.org/software/bash/" target="_blank"> <img height="" src="https://img.shields.io/static/v1?label=&message=GNU%20Bash&color=4EAA25&logo=GNU%20Bash&logoColor=4EAA25&labelColor=2F333A" alt="terminal"></a> <!-- python--> <a href="https://www.python.org" target="_blank"> <img height="" src="https://img.shields.io/static/v1?label=&message=Python&color=FFD43B&logo=python&logoColor=3776AB&labelColor=2F333A" alt="python"></a> </a> <!-- vim --> <a href="https://www.vim.org/" target="_blank"> <img height="" src="https://img.shields.io/static/v1?label=&message=Vim&color=019733&logo=Vim&logoColor=019733&labelColor=2F333A" alt="Suite CRM"></a> <!-- vs code --> <a href="https://code.visualstudio.com/" target="_blank"> <img height="" src="https://img.shields.io/static/v1?label=&message=Visual%20Studio%20Code&color=5C2D91&logo=Visual%20Studio%20Code&logoColor=5C2D91&labelColor=2F333A" alt="Suite CRM"></a> </a><!-- git --> <a href="https://git-scm.com/" target="_blank"> <img height="" src="https://img.shields.io/static/v1?label=&message=Git&color=F05032&logo=Git&logoColor=F05032&labelColor=2F333A" alt="git distributed version control system"></a> <!-- github --> <a href="https://github.com" target="_blank"> <img height="" src="https://img.shields.io/static/v1?label=&message=GitHub&color=181717&logo=GitHub&logoColor=f2f2f2&labelColor=2F333A" alt="Github"></a>
 <!-- Style guidelines -->
* Style guidelines:
  * [pycodestyle (version 2.7.*)](https://pypi.org/project/pycodestyle/)
  * [PEP8](https://pep8.org/)

All the development and testing was runned over an operating system Ubuntu 20.04 LTS using programming language Python 3.8.3. The editors used were VIM 8.1.2269, VSCode 1.6.1 and Atom 1.58.0 . Control version using Git 2.25.1.

## 0x03 Installation

* Clone this repository: `git clone "https://github.com/Abdeljalil37/AirBnB_clone.git"`
* Access AirBnb directory: `cd AirBnB_clone`
* Run hbnb(interactively): `./console` and enter command
* Run hbnb(non-interactively): `echo "<command>" | ./console.py`

#### Functionalities of this command interpreter:
* Create a new object (ex: a new User or a new Place)
* Retrieve an object from a file, a database etc...
* Do operations on objects (count, compute stats, etc...)
* Update attributes of an object
* Destroy an object

change to the `AirBnb` directory and run the command:

```bash
 ./console.py
```

### Execution

In interactive mode

```bash
$ ./console.py
(hbnb) help

Documented commands (type help <topic>):
========================================
EOF  help  quit

(hbnb)
(hbnb)
(hbnb) quit
$
```

in Non-interactive mode

```bash
$ echo "help" | ./console.py
(hbnb)

Documented commands (type help <topic>):
========================================
EOF  help  quit
(hbnb)
$
$ cat test_help
help
$
$ cat test_help | ./console.py
(hbnb)

Documented commands (type help <topic>):
========================================
EOF  help  quit
(hbnb)
$
```

## 0x04 Testing

All the test are defined in the `tests` folder.

### Documentation

* Modules:

```python
python3 -c 'print(__import__("my_module").__doc__)'
```

* Classes:

```python
python3 -c 'print(__import__("my_module").MyClass.__doc__)'
```

* Functions (inside and outside a class):

```python
python3 -c 'print(__import__("my_module").my_function.__doc__)'
```

and

```python
python3 -c 'print(__import__("my_module").MyClass.my_function.__doc__)'
```

### Python Unit Tests

* unittest module
* File extension ``` .py ```
* Files and folders star with ```test_```
* Organization:for ```models/base.py```, unit tests in: ```tests/test_models/test_base.py```
* Execution command: ```python3 -m unittest discover tests```
* or: ```python3 -m unittest tests/test_models/test_base.py```

### run test in interactive mode

```bash
echo "python3 -m unittest discover tests" | bash
```

### run test in non-interactive mode

To run the tests in non-interactive mode, and discover all the test, you can use the command:

```bash
python3 -m unittest discover tests
```


## 0x05 Usage


```bash 
$ echo "help" | ./console.py
(hbnb) 
Documented commands (type help <topic>):
========================================
EOF  all  count  create  destroy  help  quit  show  update

(hbnb) 
$
```

Alternatively, to use the AirBnB_clone console in interactive mode, run the 
file `console.py` by itself:

```bash
$ ./console.py
```

While running in interactive mode, the console displays a prompt for input:

```bash
$ ./console.py
(hbnb) 
```

To quit the console, enter the command `quit`, or input an EOF signal 
(`ctrl-D`).

```bash
$ ./console.py
(hbnb) quit
$
```

```bash
$ ./console.py
(hbnb) EOF
$
```
```

```
### Console Commands

The AirBnB console supports the following commands:

* **create**
  * Usage: `create <class>`

Creates a new instance of a given class. The class' ID is printed and 
the instance is saved to the file `file.json`.

```
$ ./console.py
(hbnb) create BaseModel
119be863-6fe5-437e-a180-b9892e8746b8
(hbnb) quit
$ cat file.json ; echo ""
{"BaseModel.119be863-6fe5-437e-a180-b9892e8746b8": {"updated_at": "2019-02-17T2
1:30:42.215277", "created_at": "2019-02-17T21:30:42.215277", "__class__": "Base
Model", "id": "119be863-6fe5-437e-a180-b9892e8746b8"}}
```

* **show**
  * Usage: `show <class> <id>` or `<class>.show(<id>)`

Prints the string representation of a class instance based on a given id.

```
$ ./console.py
(hbnb) create User
1e32232d-5a63-4d92-8092-ac3240b29f46
(hbnb)
(hbnb) show User 1e32232d-5a63-4d92-8092-ac3240b29f46
[User] (1e32232d-5a63-4d92-8092-ac3240b29f46) {'id': '1e32232d-5a63-4d92-8092-a
c3240b29f46', 'created_at': datetime.datetime(2019, 2, 17, 21, 34, 3, 635828), 
'updated_at': datetime.datetime(2019, 2, 17, 21, 34, 3, 635828)}
(hbnb) 
(hbnb) User.show(1e32232d-5a63-4d92-8092-ac3240b29f46)
[User] (1e32232d-5a63-4d92-8092-ac3240b29f46) {'id': '1e32232d-5a63-4d92-8092-a
c3240b29f46', 'created_at': datetime.datetime(2019, 2, 17, 21, 34, 3, 635828), 
'updated_at': datetime.datetime(2019, 2, 17, 21, 34, 3, 635828)}
(hbnb) 
```
* **destroy**
  * Usage: `destroy <class> <id>` or `<class>.destroy(<id>)`

Deletes a class instance based on a given id. The storage file `file.json` 
is updated accordingly.

```
$ ./console.py
(hbnb) create State
d2d789cd-7427-4920-aaae-88cbcf8bffe2
(hbnb) create Place
3e-8329-4f47-9947-dca80c03d3ed
(hbnb)
(hbnb) destroy State d2d789cd-7427-4920-aaae-88cbcf8bffe2
(hbnb) Place.destroy(03486a3e-8329-4f47-9947-dca80c03d3ed)
(hbnb) quit
$ cat file.json ; echo ""
{}
```

* **all**
  * Usage: `all` or `all <class>` or `<class>.all()`

Prints the string representations of all instances of a given class. If no 
class name is provided, the command prints all instances of every class.

```
$ ./console.py
(hbnb) create BaseModel
fce2124c-8537-489b-956e-22da455cbee8
(hbnb) create BaseModel
450490fd-344e-47cf-8342-126244c2ba99
(hbnb) create User
b742dbc3-f4bf-425e-b1d4-165f52c6ff81
(hbnb) create User
8f2d75c8-fb82-48e1-8ae5-2544c909a9fe
(hbnb)
(hbnb) all BaseModel
["[BaseModel] (450490fd-344e-47cf-8342-126244c2ba99) {'updated_at': datetime.da
tetime(2019, 2, 17, 21, 45, 5, 963516), 'created_at': datetime.datetime(2019, 2
, 17, 21, 45, 5, 963516), 'id': '450490fd-344e-47cf-8342-126244c2ba99'}", "[Bas
eModel] (fce2124c-8537-489b-956e-22da455cbee8) {'updated_at': datetime.datetime
(2019, 2, 17, 21, 43, 56, 899348), 'created_at': datetime.datetime(2019, 2, 17,
21, 43, 56, 899348), 'id': 'fce2124c-8537-489b-956e-22da455cbee8'}"]
(hbnb)
(hbnb) User.all()
["[User] (8f2d75c8-fb82-48e1-8ae5-2544c909a9fe) {'updated_at': datetime.datetim
e(2019, 2, 17, 21, 44, 44, 428413), 'created_at': datetime.datetime(2019, 2, 17
, 21, 44, 44, 428413), 'id': '8f2d75c8-fb82-48e1-8ae5-2544c909a9fe'}", "[User] 
(b742dbc3-f4bf-425e-b1d4-165f52c6ff81) {'updated_at': datetime.datetime(2019, 2
, 17, 21, 44, 15, 974608), 'created_at': datetime.datetime(2019, 2, 17, 21, 44,
15, 974608), 'id': 'b742dbc3-f4bf-425e-b1d4-165f52c6ff81'}"]
(hbnb) 
(hbnb) all
["[User] (8f2d75c8-fb82-48e1-8ae5-2544c909a9fe) {'updated_at': datetime.datetim
e(2019, 2, 17, 21, 44, 44, 428413), 'created_at': datetime.datetime(2019, 2, 17
, 21, 44, 44, 428413), 'id': '8f2d75c8-fb82-48e1-8ae5-2544c909a9fe'}", "[BaseMo
del] (450490fd-344e-47cf-8342-126244c2ba99) {'updated_at': datetime.datetime(20
19, 2, 17, 21, 45, 5, 963516), 'created_at': datetime.datetime(2019, 2, 17, 21,
45, 5, 963516), 'id': '450490fd-344e-47cf-8342-126244c2ba99'}", "[User] (b742db
c3-f4bf-425e-b1d4-165f52c6ff81) {'updated_at': datetime.datetime(2019, 2, 17, 2
1, 44, 15, 974608), 'created_at': datetime.datetime(2019, 2, 17, 21, 44, 15, 97
4608), 'id': 'b742dbc3-f4bf-425e-b1d4-165f52c6ff81'}", "[BaseModel] (fce2124c-8
537-489b-956e-22da455cbee8) {'updated_at': datetime.datetime(2019, 2, 17, 21, 4
3, 56, 899348), 'created_at': datetime.datetime(2019, 2, 17, 21, 43, 56, 899348
), 'id': 'fce2124c-8537-489b-956e-22da455cbee8'}"]
(hbnb) 
```

* **count**
  * Usage: `count <class>` or `<class>.count()`

Retrieves the number of instances of a given class.

```
$ ./console.py
(hbnb) create Place
12c73223-f3d3-4dec-9629-bd19c8fadd8a
(hbnb) create Place
aa229cbb-5b19-4c32-8562-f90a3437d301
(hbnb) create City
22a51611-17bd-4d8f-ba1b-3bf07d327208
(hbnb) 
(hbnb) count Place
2
(hbnb) city.count()
1
(hbnb) 
```

* **update**
  * Usage: `update <class> <id> <attribute name> "<attribute value>"` or
`<class>.update(<id>, <attribute name>, <attribute value>)` or `<class>.update(
<id>, <attribute dictionary>)`.

Updates a class instance based on a given id with a given key/value attribute 
pair or dictionary of attribute pairs. If `update` is called with a single 
key/value attribute pair, only "simple" attributes can be updated (ie. not 
`id`, `created_at`, and `updated_at`). However, any attribute can be updated by 
providing a dictionary.

```
$ ./console.py
(hbnb) create User
6f348019-0499-420f-8eec-ef0fdc863c02
(hbnb)
(hbnb) update User 6f348019-0499-420f-8eec-ef0fdc863c02 first_name "Holberton"
(hbnb) show User 6f348019-0499-420f-8eec-ef0fdc863c02
[User] (6f348019-0499-420f-8eec-ef0fdc863c02) {'created_at': datetime.datetime(
2019, 2, 17, 21, 54, 39, 234382), 'first_name': 'Holberton', 'updated_at': date
time.datetime(2019, 2, 17, 21, 54, 39, 234382), 'id': '6f348019-0499-420f-8eec-
ef0fdc863c02'}
(hbnb)
(hbnb) User.update(6f348019-0499-420f-8eec-ef0fdc863c02, address, "98 Mission S
t")
(hbnb) User.show(6f348019-0499-420f-8eec-ef0fdc863c02)
[User] (6f348019-0499-420f-8eec-ef0fdc863c02) {'created_at': datetime.datetime(
2019, 2, 17, 21, 54, 39, 234382), 'address': '98 Mission St', 'first_name': 'Ho
lberton', 'updated_at': datetime.datetime(2019, 2, 17, 21, 54, 39, 234382), 'id
': '6f348019-0499-420f-8eec-ef0fdc863c02'}
(hbnb)
(hbnb) User.update(6f348019-0499-420f-8eec-ef0fdc863c02, {'email': 'holberton@h
olberton.com', 'last_name': 'School'})
[User] (6f348019-0499-420f-8eec-ef0fdc863c02) {'email': 'holberton@holberton.co
m', 'first_name': 'Holberton', 'updated_at': datetime.datetime(2019, 2, 17, 21,
54, 39, 234382), 'address': '98 Mission St', 'last_name': 'School', 'id': '6f34
8019-0499-420f-8eec-ef0fdc863c02', 'created_at': datetime.datetime(2019, 2, 17,
21, 54, 39, 234382)}
(hbnb) 
```

## Testing :straight_ruler:

Unittests for the AirBnB_clone project are defined in the [tests](./tests) 
folder. To run the entire test suite simultaneously, execute the following command:

```
$ python3 unittest -m discover tests
```

Alternatively, you can specify a single test file to run at a time:

```
$ python3 unittest -m tests/test_console.py
```

## Bugs
No known bugs at this time. 

## 0x06 Authors

<details>
    <summary>EzzagmounyAZIZ</summary>
    <ul>
    <li><a href="https://github.com/EzzagmounyAZIZ">Github</a></li>
    </ul>
</details>
<details>
    <summary>Yassine Filali</summary>
    <ul>
    <li><a href="https://github.com/Yassine055">Github</a></li>
    </ul>
</details>
