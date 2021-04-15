# Linux


### 1: find files
  ? - > поиск по одному символу
  
  ?? -> два символа
  
  и т.д
 
1)Example:
 
    echo ????
 Res:
 
    srcs

2)Example:
 
    echo sr??
 Res:
 
    srcs
 
### 2: "[]"
  "[]" ->  последовательность символов 
  
  [a-k] -> от a до k
 
### 3: "{...}"

   "Множество" -> 
   пример {a..z}
   
    ls file.{f,g}.*
    
   ИЛИ
   
    for i in {a..z} ; do echo $i ; done
