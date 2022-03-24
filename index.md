# Assignment1
## My meme!

![my_meme](https://user-images.githubusercontent.com/102283151/159869815-51c411e6-f319-43d4-be22-63596c7739a3.png)
```
library(magick)

sleepy_cat <- image_read("https://cdn.pixabay.com/photo/2017/09/09/09/11/cat-2731418_960_720.jpg") %>% 
  image_scale(500)

confused_cat <- image_read("https://i.pinimg.com/originals/07/9c/3e/079c3ea0dce59cc171629800294b0f3d.jpg?w=144") %>% 
  image_scale(500)

happy_cat <- image_read("https://static.boredpanda.com/blog/wp-content/uploads/2015/09/Happy-Cats__880.jpg") %>% 
  image_scale(500)

first_text <- image_blank(width = 500, height = 500, color = "#000000") %>% 
  image_annotate(text = "Watching\nonline lectures", color = "#FFFFFF", size = 50, font = "Impact", 
                 gravity = "center")

second_text <- image_blank(width = 500, height = 500, color = "#000000") %>% 
  image_annotate(text = "Attending\nlectures at Uni", color = "#FFFFFF", 
                 size = 50, font = "Impact", gravity = "center")
third_text <- image_blank(width = 500, height = 500, color = "#000000") %>% 
  image_annotate(text = "Watching lecture\nrecordings in bed", color = "#FFFFFF", size = 50, 
                 font = "Impact", gravity = "center")

first_row <- c(sleepy_cat, first_text) %>%
  image_append()

second_row <- c(confused_cat, second_text) %>%
  image_append()

third_row <- c(happy_cat, third_text) %>%
  image_append()

meme <- c(first_row, second_row, third_row) %>% 
  image_append(stack = TRUE)

image_write(meme, "my_meme.png")
```
* The motivation behind this meme is through the experience of online uni life due to the pandemics and my personal preferences when it comes to attending lectures.
* By using the classic format the memes, I was able to portray the **expressions** through the images, and the *thoughts* behind it through the text!
