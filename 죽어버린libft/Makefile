# **************************************************************************** #
#                                                                              #
#                                                         :::      ::::::::    #
#    Makefile                                           :+:      :+:    :+:    #
#                                                     +:+ +:+         +:+      #
#    By: jiyoulee <jiyoulee@student.42seoul.kr      +#+  +:+       +#+         #
#                                                 +#+#+#+#+#+   +#+            #
#    Created: 2021/06/12 16:11:16 by jiyoulee          #+#    #+#              #
#    Updated: 2021/06/12 16:14:19 by jiyoulee         ###   ########.fr        #
#                                                                              #
# **************************************************************************** #

CC			= gcc

FLAGS		= -Wall -Wextra -Werror

NAME		= libft.a

SRCS		=  ft_atoi.c ft_bzero.c ft_calloc.c ft_isalnum.c ft_isascii.c ft_isalpha.c ft_isdigit.c ft_isprint.c ft_itoa.c ft_memccpy.c ft_memchr.c ft_memcmp.c ft_memcpy.c ft_memmove.c ft_memset.c ft_putchar_fd.c ft_putendl_fd.c ft_putnbr_fd.c ft_putstr_fd.c ft_split.c ft_strchr.c ft_strdup.c ft_strjoin.c ft_strlcat.c ft_strlcpy.c ft_strlen.c ft_strmapi.c ft_strncmp.c ft_strnstr.c ft_strrchr.c ft_strtrim.c ft_substr.c ft_tolower.c ft_toupper.c\

SRCB		= ft_lstnew.c ft_lstadd_front.c ft_lstsize.c ft_lstlast.c ft_lstadd_back.c ft_lstdelone.c ft_lstclear.c ft_lstiter.c ft_lstmap.c\

OBJS		= $(SRCS:.c=.o)

OBJB		= $(SRCB:.c=.o)

ifdef WITH_BONUS
	OBJ_FILES = $(OBJS) $(OBJB)
else
	OBJ_FILES = $(OBJS)
endif

all	: $(NAME)

%.o : %.c
	$(CC) $(FLAGS) -c $< -o $@

$(NAME)	: $(OBJ_FILES)
	    ar -rcs $(NAME) $(OBJ_FILES)

bonus	: 
	@sleep 1
	@make WITH_BONUS=1 all

clean	:
	rm -f $(OBJS) $(OBJB)

fclean	: clean
	rm -f $(NAME)

re	: fclean all

.PHONY:	all bonus clean fclean re
