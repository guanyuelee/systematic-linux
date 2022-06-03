<!--
 * @Author       : Guanyue li
 * @Date         : 2022-06-03 11:54:45
 * @LastEditTime : 2022-06-03 13:43:04
 * @Description  : file content
 * @FilePath     : \systematic-linux\Input&Output.md
-->
# Linux Input and Output Redirection

Please Refer to [Guru99][1] for a complete tutorial.

> Redirection is a feature in Linux such that when executing a command, you can change the standard input/output devices. The basic workflow of any Linux command is that it takes an input and give an output.
> <ul>
> <li> The standard input (stdin) device is the keyboard. </li>
> <li> The standard output (stdout) device is the screen. </li>
> </ul>
> With redirection, the above standard input/output can be changed.
> 
> --- <cite> [Guru99][1] </cite>

```bash
# Create necessary files for testing
mkdir ABC Documents
ls -al  # check the file mode
chmod u-rwx ABC  # remove

# List the files to `dir-content` and output the error to `error-content`
ls -al ABC Documents > dir-content 2> error-content  

# Output: 
# > Documents:
# > total 8
# > drwxrwxr-x 2 student student 4096 6月   3 12:13 .
# > drwxrwxr-x 5 student student 4096 6月   3 12:14 ..
# > ls: cannot open directory 'ABC': Permission denied

ls -al ABC Documents > all-content 2>& 1
```

[1]: https://www.guru99.com/linux-redirection.html