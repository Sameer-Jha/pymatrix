#! /usr/bin/env python

# imports and libraries
from time import sleep
from os import get_terminal_size
from string import printable
from random import randint
from colorama import init, Fore, Back, Style


# initializing colorama
init()

# get terminal size
col, lines = get_terminal_size()

# compiling colors
colors = [Fore.RED, Fore.GREEN, Fore.YELLOW, Fore.BLUE, Fore.MAGENTA, Fore.CYAN, Fore.WHITE, Fore.RESET]
color_num = len(colors)

# generating charachter_list
a='qwertyuiopasdfghjklzxcvbnm'
A='QWERTYUIOPASDFGHJKLZXCVBNM'
c='абвгдежзиклмнопрстуфхцчшщъыьэюя'
C='АБВГДЕЖЗИКЛМНОПРСТУФХЦЧШЩЪЫЬЭЮЯ'
e='☺☻✌♡♥❤⚘❀❃❁✼☀✌♫♪☃❄❅❆☕☂★'
g='αβγδεζηθικλμνξοπρστυφχψως'
G='ΑΒΓΔΕΖΗΘΙΚΛΜΝΞΟΠΡΣΤΥΦΧΨΩ'
k='ｦｧｨｩｪｫｬｭｮｯｰｱｲｳｴｵｶｷｸｹｺｻｼｽｾｿﾀﾁﾂﾃﾄﾅﾆﾇﾈﾉﾊﾋﾌﾍﾎﾏﾐﾑﾒﾓﾔﾕﾖﾗﾘﾙﾚﾛﾜﾝ'
m='ｦｧｨｩｪｫｬｭｮｯｰｱｲｳｴｵｶｷｸｹｺｻｼｽｾｿﾀﾁﾂﾃﾄﾅﾆﾇﾈﾉﾊﾋﾌﾍﾎﾏﾐﾑﾒﾓﾔﾕﾖﾗﾘﾙﾚﾛﾜﾝ1234567890'
n='1234567890'
o='qwertyuiopasdfghjklzxcvbnmQWERTYUIOPASDFGHJKLZXCVBNM1234567890'
r='mcclllxxxxvvvvviiiiii'
R='MCCLLLXXXXVVVVVIIIIII'
s='-=*_+|:<>"'
S='`-=~!@#$%^&*()_+[]|\;\':",./<>?"'
char_list = a+A+c+C+e+g+G+k+m+n+o+r+R+s+S
char_list_len = len(char_list)


# abstracting operations into functions

def rcolor():       #random colorgen
    return colors[randint(0,color_num-1)]


def rchar():    # random chargen
    return (char_list[randint(0,char_list_len-1)],' ','\t')[randint(0,2)]

def main():
    # printing onto terminal
    while(1):
        for i in range(col):
            print(rcolor() + rchar(),end='')
        sleep(0.08)
        print()


# Calling main
if __name__ == "__main__":
    main()


