# 0x04. Loops, conditions and parsing 

<div style="text-align: justify">

Thank you for visiting this repository which contain our work to start learning C language programming. In this project, I learned about hashing by implementing hash functions and hash tables in C.	


![Logo](https://www.howtogeek.com/wp-content/uploads/2021/05/laptop-with-terminal-big.png?height=200p&trim=2,2,2,50)

# Getting Started :running:
<div style="text-align: justify">

## Table of Contents
* [AUTHORS](./AUTHORS)
* [MIT License](./LICENSE)
* [About](#about)
* [Dependences](#dependences)
* [Installing, compiling and using](#installing, compiling and using)
* [Builtins](#builtins)
* [Man page]
* [Credits](#credits)

## About
This directory contains a collection of files, functions, structs and scripts used to build and manage this repository. If there are any issues regarding the intention of a particular script (or even part of a certain script), please reach out to us.
	
	Contents:

- What is a hash function

- What makes a good hash function

- What is a hash table, how do they work and how to use them

- What is a collision and what are the main ways of dealing with collisions in the context of a hash table

- What are the advantages and drawbacks of using hash tables

- What are the most common use cases of hash tables
	
## Dependences 
	
> [hash_tables.h](https://github.com/Imanolasolo/holbertonschool-low_level_programming/blob/main/0x18-dynamic_libraries/main.h) --> Header file containing all functions involved in project.

> [README.md](https://github.com/Imanolasolo/holbertonschool-low_level_programming/blob/main/0x18-dynamic_libraries/README.md) ---> README file to show the project insights. 

>[0-hash_table_create.c](https://github.com/Imanolasolo/holbertonschool-low_level_programming/blob/main/0x18-dynamic_libraries/libdynamic.so) ---> function that creates a hash table.

>[1-djb2.c](https://github.com/Imanolasolo/holbertonschool-higher_level_programming/blob/master/0x04-python-more_data_structures/2-uniq_add.py) ---> hash function implementing the djb2 algorithm.

>[2-key_index.c]() --> function that gives you the index of a key.

>[3-hash_table_set.c]() --> function that adds an element to the hash table.

>[4-hash_table_get.c]() --> function that retrieves a value associated with a key.

>[5-hash_table_print.c]() --> function that prints a hash table.

>[6-hash_table_delete.c]() --> function that deletes a hash table. 

>[100-sorted_hash_table.c]() --> Rewrite the previous functions using these data structures:

```
shash_table_t *shash_table_create(unsigned long int size);

int shash_table_set(shash_table_t *ht, const char *key, const char *value);

char *shash_table_get(const shash_table_t *ht, const char *key);

void shash_table_print(const shash_table_t *ht);

void shash_table_print_rev(const shash_table_t *ht);

void shash_table_delete(shash_table_t *ht);
```

## Installing, compiling and using
	
> Only install cloning this repository on your local device:  https://github.com/Imanolasolo/holbertonschool-low_level_programming.git
	
> Compile the .c files with `gcc` using ` -Wall -Werror -Wextra -pedantic -std=gnu89`
	
> Run the executable files with `./` 

## Builtins
```
hash_table_t *hash_table_create(unsigned long int size);
unsigned long int hash_djb2(const unsigned char *str);
unsigned long int key_index(const unsigned char *key, unsigned long int size);
int hash_table_set(hash_table_t *ht, const char *key, const char *value);
char *hash_table_get(const hash_table_t *ht, const char *key);
void hash_table_print(const hash_table_t *ht);
void hash_table_delete(hash_table_t *ht);

```
		
## Man page

-  No man page

## Flowchart
	
- No flowchart

## Resources

**Read or watch**:

[What is a HashTable Data Structure - Introduction to Hash Tables , Part 0](https://intranet.hbtn.io/rltoken/uodWZz-2jyHReOeToaLNdQ)

[Hash function](https://intranet.hbtn.io/rltoken/YiFi_oMjd9cZ4VepsS2RKQ)

[Hash table](https://intranet.hbtn.io/rltoken/Kswyyb1f2JY3dn-3TEckUQ)


## Usage



## Credits

## Author(s):blue_book:

Work is owned and maintained by:
* Imanol Asolo <[3848](mailto:3848@holbertonschool.com)> [![M](https://upload.wikimedia.org/wikipedia/commons/thumb/9/91/Octicons-mark-github.svg/25px-Octicons-mark-github.svg.png)](https://github.com/Imanolasolo) [![M](https://upload.wikimedia.org/wikipedia/fr/thumb/c/c8/Twitter_Bird.svg/25px-Twitter_Bird.svg.png)](https://twitter.com/jjusturi) [![M](https://upload.wikimedia.org/wikipedia/commons/thumb/c/ca/LinkedIn_logo_initials.png/25px-LinkedIn_logo_initials.png)](https://www.linkedin.com/in/imanol-asolo-5ba9b42a/)


## Acknowledgments :mega: 

### **`Holberton School`** (*providing guidance*)
This program was written as part of the curriculum for Holberton School.
Holberton School is a campus-based full-stack software engineering program
that prepares students for careers in the tech industry using project-based
peer learning. For more information, visit [this link](https://www.holbertonschool.com/).
<p align="center">
	<img src="https://assets.website-files.com/6105315644a26f77912a1ada/610540e8b4cd6969794fe673_Holberton_School_logo-04-04.svg" alt="This is a secret;)">
</p>