# **************************************************************************** #
#                                                                              #
#                                                         :::      ::::::::    #
#    Makefile                                           :+:      :+:    :+:    #
#                                                     +:+ +:+         +:+      #
#    By: greita <greita@student.21-school.ru>       +#+  +:+       +#+         #
#                                                 +#+#+#+#+#+   +#+            #
#    Created: 2021/10/15 10:29:31 by greita            #+#    #+#              #
#    Updated: 2021/12/09 10:02:09 by greita           ###   ########.fr        #
#                                                                              #
# **************************************************************************** #

NAME = 		libft.a

LIST = 		ft_isdigit.c ft_isalpha.c ft_isalnum.c ft_isascii.c \
			ft_isprint.c ft_strlen.c ft_memset.c ft_bzero.c ft_memcpy.c \
			ft_memmove.c ft_strlcpy.c ft_strlcat.c ft_toupper.c \
			ft_tolower.c ft_strchr.c ft_strrchr.c ft_strncmp.c ft_memchr.c \
			ft_memcmp.c ft_strnstr.c ft_atoi.c ft_calloc.c ft_strdup.c \
			ft_substr.c ft_strjoin.c ft_strtrim.c ft_split.c ft_itoa.c \
			ft_strmapi.c ft_striteri.c ft_putchar_fd.c ft_putstr_fd.c \
			ft_putendl_fd.c ft_putnbr_fd.c

LIST_B =	ft_lstnew_bonus.c ft_lstadd_front_bonus.c ft_lstsize_bonus.c \
			ft_lstlast_bonus.c ft_lstadd_back_bonus.c ft_lstdelone_bonus.c \
			ft_lstclear_bonus.c ft_lstiter_bonus.c ft_lstmap_bonus.c

OBJ = 		$(LIST:.c=.o)

OBJ_B =		$(LIST_B:.c=.o)

CC =		gcc

FLAGS =		-Wall -Wextra -Werror -O2

D_FILES =	$(LIST:.c=.d) $(LIST_B:.c=.d)

%.o :		%.c libft.h
	$(CC) $(FLAGS) -c $< -o $@ -MMD

all :		$(NAME)

-include	$(D_FILES)

$(NAME) :	$(OBJ)
	ar rcs $(NAME) $?

bonus :
	@make OBJ="$(OBJ_B)" all

clean :
	rm -f $(OBJ) $(OBJ_B) $(D_FILES)

fclean :	clean
	rm -f $(NAME)

re :		fclean all

.PHONY :	all clean fclean re bonus
