# Notes for pip install
 First update the pip if any problems pop up

    pip install --upgrade pip

## Download speed:
1. If downloading speed is too slow, try a _different source_ temporarily
    > Reference: https://blog.csdn.net/qq595662096/article/details/93846417
    
      pip install <name> -i https://pypi.tuna.tsinghua.edu.cn/simple

    Then we can change the pip source



## Errors
1. If `MemoryError`
    > Reference: https://stackoverflow.com/questions/29466663/memory-error-while-using-pip-install-matplotlib

    Try add this in the command

       -no-cache-dir

