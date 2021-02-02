OBJ=test.o
PCSRC=test.pc
SRC=test.c
CC=gcc
PROC=proc

LDLIB=/$(ORACLE_HOME)/lib  

FLAGS=-ldl -lm -lclntsh


TARGET=test


$(TARGET) : $(OBJ) 
	$(CC) -o $(TARGET) $(OBJ) -L$(LDLIB) $(FLAGS)

$(OBJ) : $(SRC)
	$(CC) -c $(SRC)

$(SRC) : $(PCSRC)
	$(PROC) $(PCSRC)

clean :
	rm -rf $(OBJ) $(SRC) $(TARGET) *.lis

all : $(TARGET)
