#######################################################################
#                                                                     #
# Makefile for rns.c (version 1.0), March 1995, Unix version          #
#                                                                     #      
# Edit items 1-3.                                                     #      
#                                                                     #      
#######################################################################
#                                                                     #
# 1. Specify C compiler and ANSI option:                              #
#                                                                     #      
####################################################################### 

CC=cc -std1

#######################################################################
#                                                                     #
# 2. Specify compiling options:                                       # 
#                                                                     #      
####################################################################### 

fast:=OPTION=-O -Olimit 1200
debug:=OPTION=-g  
profile:=OPTION=-p 

#######################################################################
#                                                                     #
# 3. Specify grid size (optional):                                    # 
#                                                                     #      
####################################################################### 

#STANDARD
SIZE=-DMDIV=65 -DSDIV=129

#HIGH
#SIZE=-DMDIV=101 -DSDIV=201

#VERY HIGH
#SIZE=-DMDIV=151 -DSDIV=301

#LOW
#SIZE=-DMDIV=51 -DSDIV=101
 

#######################################################################
#                                                                     #
# 4. Specify number of terms in polynomial expansion (optional):      # 
#                                                                     #      
####################################################################### 
 
LM=-DLMAX=10
 

#######################################################################
#                                                                     #
# Make:                                                               # 
#                                                                     #      
####################################################################### 

fast:rns

debug:rns

profile:rns

rns: rns.o
	$(CC) $(OPTION) $(SIZE) $(LM) -lm -o rns rns.o 
rns.o: rns.c
	$(CC) -c   $(OPTION)  $(SIZE) $(LM) rns.c

