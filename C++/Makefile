#CXX=g++-12
SRC=$(wildcard *.cpp)  
NAME=main
BIN_DIR = bin
BUILD_DIR = build

CXXFLAGS+=-Wall -Wextra -MMD -g -fdiagnostics-color=auto
LDFLAGS= #-lSDL

OBJ=$(addprefix $(BUILD_DIR)/,$(SRC:.cpp=.o))
DEP=$(addprefix $(BUILD_DIR)/,$(SRC:.cpp=.d))

$(BIN_DIR)/$(NAME): $(OBJ)
	@mkdir -p $(BIN_DIR)
	$(CXX) -o $@ $^ $(LDFLAGS)

$(BUILD_DIR)/%.o: %.cpp
	@mkdir -p $(BUILD_DIR)
	$(CXX) $(CXXFLAGS) -o $@ -c $<

clean:
	rm -rf $(BUILD_DIR) $(BIN_DIR) core *.gch

-include $(DEP)
