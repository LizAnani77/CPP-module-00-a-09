# **************************************************************************** #
#                                                                              #
#                                                         :::      ::::::::    #
#    Makefile                                           :+:      :+:    :+:    #
#                                                     +:+ +:+         +:+      #
#    By: claude             <span class="math-inline">\+         \+</span>      #
#                                                 +#+#+#+#+#+   +#+            #
#    Created: 2024/12/30 by claude                     #+#    #+#             #
#    Updated: 2024/12/30 by claude                    ###   ########.fr        #
#                                                                              #
# **************************************************************************** #

CLEAN_COLOR     =   \033[38;5;201m
REMOVE_COLOR    =   \033[38;5;207m
COMPILE_COLOR   =   \033[38;5;213m
BOX_COLOR       =   \033[38;5;225m

RESET           =   \033[0m

NAME            =   harlFilter

CC              =   c++
CFLAGS          =   -Wall -Wextra -Werror -std=c++98

SRCS            =   main.cpp Harl.cpp
OBJS            =   $(SRCS:.cpp=.o)

all:            $(NAME)

$(NAME): $(OBJS)
	@echo "$(BOX_COLOR)╔════════════════════════════════════════════════╗$(RESET)"
	@echo "$(BOX_COLOR)║              Compiling $(NAME)...           ║$(RESET)"
	@$(CC) $(CFLAGS) -o $(NAME) $(OBJS)
	@echo "$(BOX_COLOR)║    $(NAME) has been created successfully!   ║$(RESET)"
	@echo "$(BOX_COLOR)╚════════════════════════════════════════════════╝$(RESET)"

%.o: %.cpp
	@echo "$(COMPILE_COLOR)▶ Compiling: $<$(RESET)"
	@$(CC) $(CFLAGS) -c $< -o $@

clean:
	@echo "$(CLEAN_COLOR)🧹 Cleaning object files...$(RESET)"
	@rm -f $(OBJS)

fclean: clean
	@echo "$(REMOVE_COLOR)🗑️  Removing $(NAME)...$(RESET)"
	@rm -f $(NAME)

re: fclean all

.PHONY: all clean fclean re