##
## EPITECH PROJECT, 2018
## arcade
## File description:
## Makefile for a Pacman game.
##

CXX		?=	g++

SRC		=	Pacman.cpp		\
			Perso.cpp		\
			drawMap.cpp		\
			Ghost.cpp

SRC		:=	$(addprefix src/, $(SRC))

OBJ		=	$(SRC:.cpp=.o)

CPPFLAGS	+=	-I include -I ../../core/include

CXXFLAGS	+=	-Wall -Wextra -fPIC

NAME		=	../../games/lib_arcade_pacman.so

all: $(NAME)

$(NAME): $(OBJ)
	$(CXX) -shared -o $(NAME) $(OBJ) $(LDFLAGS)

clean:
	$(RM) $(OBJ)

fclean: clean
	$(RM) $(NAME)

re: fclean all

.PHONY: all clean fclean re test
