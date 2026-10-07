# std::string notes

Is C++'s dynamic way of dealing with char arrays. It tracks its own size and capacity. it alsow supports copying moving concatenations, searching and substring extraction.

Short strings tend to be allocated directly on the object.

Some things to look out for. When capacity is exceeded the entire string is reallocated elsewhere and usually doubles in size.

Copying tends to duplicate the contents wheras moving transfers ownership but does not copy.

has most of the same time complexity for actions as a standard vector.

string view is the pointer version that just saves the char* and size useful when you don't want to accidentally move memory around using string. 