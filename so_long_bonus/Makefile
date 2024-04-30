NAME = so_long_bonus

SRCS =	so_long_bonus.c so_long_utils_bonus.c so_long_map_bonus.c \
		get_next_line_bonus.c get_next_line_utils_bonus.c \
		errors_bonus.c sprites_bonus.c keyboard_bonus.c ft_itoa_bonus.c

OBJECTS = $(SRCS:.c=.o)

CFLAGS := -Wall -Wextra -Werror -Imlx 
REMOVE = rm -f
CC := cc

all: $(NAME)

$(NAME): $(OBJECTS) printf/libftprintf.a mlx/libmlx.a
	$(CC) $(OBJECTS) printf/libftprintf.a -Lmlx -lmlx -framework OpenGL -framework AppKit -o $(NAME)

mlx/libmlx.a:
	make -C mlx/

printf/libftprintf.a:
	make -C printf/

run:
	./so_long map1.ber

clean:
	$(REMOVE) $(OBJECTS)
	$(REMOVE) $(OBJECTS_BONUS)
	make -C mlx/ clean
	make -C printf/ fclean

fclean: clean
	$(REMOVE) $(NAME)
	$(REMOVE) $(NAME_BONUS)

re: fclean all