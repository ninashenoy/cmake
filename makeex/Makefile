INC_DIR=inc
SRC_DIR=src
OBJ_DIR=build
CC=g++

app: $(OBJ_DIR)/main.o $(OBJ_DIR)/add.o $(OBJ_DIR)/sub.o
	$(CC) -o $(OBJ_DIR)/app $(OBJ_DIR)/main.o $(OBJ_DIR)/sub.o $(OBJ_DIR)/add.o

$(OBJ_DIR)/main.o: $(SRC_DIR)/main.cpp
	$(CC) -o $(OBJ_DIR)/main.o -I $(INC_DIR) -c $(SRC_DIR)/main.cpp

$(OBJ_DIR)/add.o: $(SRC_DIR)/add.cpp
	$(CC) -o $(OBJ_DIR)/add.o -I $(INC_DIR) -c $(SRC_DIR)/add.cpp

$(OBJ_DIR)/sub.o: $(SRC_DIR)/sub.cpp
	$(CC) -o $(OBJ_DIR)/sub.o -I $(INC_DIR) -c $(SRC_DIR)/sub.cpp

clean:
	rm -rf $(OBJ_DIR)/
	ls -la

run:
	$(OBJ_DIR)/app

$(shell mkdir -p $(OBJ_DIR)) 
