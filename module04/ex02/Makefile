# **************************************************************************** #
#                                                                              #
#                                                         :::      ::::::::    #
#    Makefile                                           :+:      :+:    :+:    #
#                                                     +:+ +:+         +:+      #
#    By: lanani-f <lanani-f@student.42.fr>          +#+  +:+       +#+         #
#                                                 +#+#+#+#+#+   +#+            #
#    Created: 2024/01/03 21:33:40 by lanani-f          #+#    #+#             #
#    Updated: 2024/01/03 21:34:08 by lanani-f         ###   ########.fr       #
#                                                                              #
# **************************************************************************** #

CLEAN_COLOR 	= 	\033[38;5;196m
REMOVE_COLOR 	= 	\033[38;5;202m
COMPILE_COLOR 	= 	\033[38;5;208m
BOX_COLOR 		= 	\033[38;5;214m
RESET 			= 	\033[0m

NAME			=	abstract
CC				=	c++
CFLAGS			=	-Wall -Wextra -Werror -std=c++98
SRCS			=	main.cpp Animal.cpp Dog.cpp Cat.cpp Brain.cpp
OBJS			=	$(SRCS:.cpp=.o)

all:			$(NAME)

$(NAME):		$(OBJS)
	@echo "$(BOX_COLOR)╔════════════════════════════════════════════╗$(RESET)"
	@echo "$(BOX_COLOR)║            Compiling $(NAME)...           ║$(RESET)"
	@$(CC) $(CFLAGS) -o $(NAME) $(OBJS)
	@echo "$(BOX_COLOR)║  $(NAME) has been created successfully!   ║$(RESET)"
	@echo "$(BOX_COLOR)╚════════════════════════════════════════════╝$(RESET)"

%.o:			%.cpp
	@echo "$(COMPILE_COLOR)▶ Compiling: $<$(RESET)"
	@$(CC) $(CFLAGS) -c $< -o $@

clean:
	@echo "$(CLEAN_COLOR)🧹 Cleaning object files...$(RESET)"
	@rm -f $(OBJS)

fclean:			clean
	@echo "$(REMOVE_COLOR)🗑️  Removing $(NAME)...$(RESET)"
	@rm -f $(NAME)

re:				fclean all

.PHONY:			all clean fclean re