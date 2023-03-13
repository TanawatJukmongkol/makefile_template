# **************************************************************************** #
#                                                                              #
#                                                         :::      ::::::::    #
#    Makefile                                           :+:      :+:    :+:    #
#                                                     +:+ +:+         +:+      #
#    By: tjukmong <tjukmong@student.42bangkok.co    +#+  +:+       +#+         #
#                                                 +#+#+#+#+#+   +#+            #
#    Created: 2023/03/12 18:41:41 by yourname          #+#    #+#              #
#    Updated: 2023/03/13 15:29:42 by tjukmong         ###   ########.fr        #
#                                                                              #
# **************************************************************************** #

NAME		= orbit4
MAIN		= main.c
MAIN_DIR	= ./

CC			= gcc
CFLAG		= -g -Wall -Werror -Wextra

SRC_DIR		= ./src/

MODULE1		= orbit4.c orbit42.c
MODULE2		= orbit43.c orbit44.c
MODULE3		= module3.c

MODULE1_DIR	= ./src/module1/
MODULE2_DIR = ./src/module2/
MODULE3_DIR = ./src/module3/

LIB_DIR		= ./lib/

OBJ_DIR		= ./obj/

OBJS		= ${addprefix $(OBJ_DIR),$(MODULE1:.c=.o)} \
			  ${addprefix $(OBJ_DIR),$(MODULE2:.c=.o)} \
			  ${addprefix $(OBJ_DIR),$(MODULE3:.c=.o)} \
			  ${addprefix $(OBJ_DIR),$(MAIN:.c=.o)}

RM = rm -rf

${OBJ_DIR}%.o: ${MODULE1_DIR}%.c
	$(CC) -c -o $@ $^

${OBJ_DIR}%.o: ${MODULE2_DIR}%.c
	$(CC) -c -o $@ $^

${OBJ_DIR}%.o: ${MODULE3_DIR}%.c
	$(CC) -c -o $@ $^

all: ${OBJ_DIR} ${NAME}

${OBJ_DIR}:
	mkdir -p $(OBJ_DIR)

${OBJ_DIR}%.o: ${MAIN_DIR}%.c
	$(CC) -c -o $@ $^

${NAME}: ${OBJS}
	$(CC) $(OBJS) -o $(NAME) $(CFLAG)

clean:
	$(RM) $(OBJ_DIR)
fclean: clean
	$(RM) $(NAME)
re: fclean all
