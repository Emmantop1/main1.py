def read_file_content(filename):
    with open(filename) as file:
        read_content= file.read()
    return read_content



def count_word():
    text=read_file_content("C:/Users/user/Downloads/Reading-Text-Files/story.txt")
    text=text.translate(str.maketrans('', '', string.punctuation))
    word_count={}
    split_text=text.split()

    for word in split_text:
        word_count[word] =split_text.count(word)


print(count_word())
