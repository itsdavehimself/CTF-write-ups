# picoCTF Some Assembly Required 1

## Description
http://mercury.picoctf.net:26318/index.html

## Not Much to Go Off
Since there's not much to go off. I figured I'd inspect the page. In the sources file, I spent some time inspecting the JS code. In the array, I noticed an element './JIFxzHyW8W' which looked like a path. So I followed that to http://mercury.picoctf.net:26318/JIFxzHyW8W.'

This page downloaded a binary file named JIFxzHyW8W.

## Strings
In the terminal, I used the strings command:

```strings JIFxzHyW8W```

I received the following output:

> memory
> __wasm_call_ctors
> strcmp
> check_flag
> input
> 	copy_char
> __dso_handle
> __data_end
> __global_base
> __heap_base
> __memory_base
> __table_base
> j!	 
>   F!!A
> !" ! "q!# #
> !% $ %q!& 
> !( ' (q!) & )k!* 
> !+ +
>  	q!
> +picoCTF{8857462f9e30faae4d037e5e25fee1ce}

## The Flag

picoCTF{8857462f9e30faae4d037e5e25fee1ce}
