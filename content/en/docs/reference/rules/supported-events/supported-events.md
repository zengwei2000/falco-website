Falco | Dir | Event
:-----|:----|:-----
Yes | > | **open**(FSPATH name, FLAGS32 flags, UINT32 mode)
Yes | < | **open**(FD fd, FSPATH name, FLAGS32 flags, UINT32 mode, UINT32 dev, UINT64 ino)
Yes | > | **close**(FD fd)
Yes | < | **close**(ERRNO res)
No | > | **read**(FD fd, UINT32 size)
No | < | **read**(ERRNO res, BYTEBUF data)
No | > | **write**(FD fd, UINT32 size)
No | < | **write**(ERRNO res, BYTEBUF data)
Yes | > | **socket**(ENUMFLAGS32 domain, UINT32 type, UINT32 proto)
Yes | < | **socket**(FD fd)
Yes | > | **bind**(FD fd)
Yes | < | **bind**(ERRNO res, SOCKADDR addr)
Yes | > | **connect**(FD fd, SOCKADDR addr)
Yes | < | **connect**(ERRNO res, SOCKTUPLE tuple)
Yes | > | **listen**(FD fd, UINT32 backlog)
Yes | < | **listen**(ERRNO res)
No | > | **send**(FD fd, UINT32 size)
No | < | **send**(ERRNO res, BYTEBUF data)
Yes | > | **sendto**(FD fd, UINT32 size, SOCKTUPLE tuple)
Yes | < | **sendto**(ERRNO res, BYTEBUF data)
No | > | **recv**(FD fd, UINT32 size)
No | < | **recv**(ERRNO res, BYTEBUF data)
Yes | > | **recvfrom**(FD fd, UINT32 size)
Yes | < | **recvfrom**(ERRNO res, BYTEBUF data, SOCKTUPLE tuple)
Yes | > | **shutdown**(FD fd, ENUMFLAGS8 how)
Yes | < | **shutdown**(ERRNO res)
No | > | **getsockname**()
No | < | **getsockname**()
No | > | **getpeername**()
No | < | **getpeername**()
Yes | > | **socketpair**(ENUMFLAGS32 domain, UINT32 type, UINT32 proto)
Yes | < | **socketpair**(ERRNO res, FD fd1, FD fd2, UINT64 source, UINT64 peer)
No | > | **setsockopt**()
No | < | **setsockopt**(ERRNO res, FD fd, ENUMFLAGS8 level, ENUMFLAGS8 optname, DYNAMIC val, UINT32 optlen)
Yes | > | **getsockopt**()
Yes | < | **getsockopt**(ERRNO res, FD fd, ENUMFLAGS8 level, ENUMFLAGS8 optname, DYNAMIC val, UINT32 optlen)
Yes | > | **sendmsg**(FD fd, UINT32 size, SOCKTUPLE tuple)
Yes | < | **sendmsg**(ERRNO res, BYTEBUF data)
No | > | **sendmmsg**()
No | < | **sendmmsg**()
Yes | > | **recvmsg**(FD fd)
Yes | < | **recvmsg**(ERRNO res, UINT32 size, BYTEBUF data, SOCKTUPLE tuple)
No | > | **recvmmsg**()
No | < | **recvmmsg**()
Yes | > | **creat**(FSPATH name, UINT32 mode)
Yes | < | **creat**(FD fd, FSPATH name, UINT32 mode, UINT32 dev, UINT64 ino)
Yes | > | **pipe**()
Yes | < | **pipe**(ERRNO res, FD fd1, FD fd2, UINT64 ino)
Yes | > | **eventfd**(UINT64 initval, FLAGS32 flags)
Yes | < | **eventfd**(FD res)
No | > | **futex**(UINT64 addr, ENUMFLAGS16 op, UINT64 val)
No | < | **futex**(ERRNO res)
No | > | **stat**()
No | < | **stat**(ERRNO res, FSPATH path)
No | > | **lstat**()
No | < | **lstat**(ERRNO res, FSPATH path)
No | > | **fstat**(FD fd)
No | < | **fstat**(ERRNO res)
No | > | **stat64**()
No | < | **stat64**(ERRNO res, FSPATH path)
No | > | **lstat64**()
No | < | **lstat64**(ERRNO res, FSPATH path)
No | > | **fstat64**(FD fd)
No | < | **fstat64**(ERRNO res)
No | > | **epoll_wait**(ERRNO maxevents)
No | < | **epoll_wait**(ERRNO res)
No | > | **poll**(FDLIST fds, INT64 timeout)
No | < | **poll**(ERRNO res, FDLIST fds)
No | > | **select**()
No | < | **select**(ERRNO res)
No | > | **select**()
No | < | **select**(ERRNO res)
No | > | **lseek**(FD fd, UINT64 offset, ENUMFLAGS8 whence)
No | < | **lseek**(ERRNO res)
No | > | **llseek**(FD fd, UINT64 offset, ENUMFLAGS8 whence)
No | < | **llseek**(ERRNO res)
No | > | **getcwd**()
No | < | **getcwd**(ERRNO res, CHARBUF path)
Yes | > | **chdir**()
Yes | < | **chdir**(ERRNO res, CHARBUF path)
Yes | > | **fchdir**(FD fd)
Yes | < | **fchdir**(ERRNO res)
No | > | **pread**(FD fd, UINT32 size, UINT64 pos)
No | < | **pread**(ERRNO res, BYTEBUF data)
No | > | **pwrite**(FD fd, UINT32 size, UINT64 pos)
No | < | **pwrite**(ERRNO res, BYTEBUF data)
No | > | **readv**(FD fd)
No | < | **readv**(ERRNO res, UINT32 size, BYTEBUF data)
No | > | **writev**(FD fd, UINT32 size)
No | < | **writev**(ERRNO res, BYTEBUF data)
No | > | **preadv**(FD fd, UINT64 pos)
No | < | **preadv**(ERRNO res, UINT32 size, BYTEBUF data)
No | > | **pwritev**(FD fd, UINT32 size, UINT64 pos)
No | < | **pwritev**(ERRNO res, BYTEBUF data)
Yes | > | **signalfd**(FD fd, UINT32 mask, FLAGS8 flags)
Yes | < | **signalfd**(FD res)
Yes | > | **kill**(PID pid, SIGTYPE sig)
Yes | < | **kill**(ERRNO res)
Yes | > | **tkill**(PID tid, SIGTYPE sig)
Yes | < | **tkill**(ERRNO res)
Yes | > | **tgkill**(PID pid, PID tid, SIGTYPE sig)
Yes | < | **tgkill**(ERRNO res)
No | > | **nanosleep**(RELTIME interval)
No | < | **nanosleep**(ERRNO res)
Yes | > | **timerfd_create**(UINT8 clockid, FLAGS8 flags)
Yes | < | **timerfd_create**(FD res)
Yes | > | **inotify_init**(FLAGS8 flags)
Yes | < | **inotify_init**(FD res)
No | > | **getrlimit**(ENUMFLAGS8 resource)
No | < | **getrlimit**(ERRNO res, INT64 cur, INT64 max)
Yes | > | **setrlimit**(ENUMFLAGS8 resource)
Yes | < | **setrlimit**(ERRNO res, INT64 cur, INT64 max)
Yes | > | **prlimit**(PID pid, ENUMFLAGS8 resource)
Yes | < | **prlimit**(ERRNO res, INT64 newcur, INT64 newmax, INT64 oldcur, INT64 oldmax)
Yes | > | **drop**(UINT32 ratio)
Yes | < | **drop**(UINT32 ratio)
Yes | > | **fcntl**(FD fd, ENUMFLAGS8 cmd)
Yes | < | **fcntl**(FD res)
No | > | **switch**(PID next, UINT64 pgft_maj, UINT64 pgft_min, UINT32 vm_size, UINT32 vm_rss, UINT32 vm_swap)
No | > | **brk**(UINT64 addr)
No | < | **brk**(UINT64 res, UINT32 vm_size, UINT32 vm_rss, UINT32 vm_swap)
No | > | **mmap**(UINT64 addr, UINT64 length, FLAGS32 prot, FLAGS32 flags, FD fd, UINT64 offset)
No | < | **mmap**(UINT64 res, UINT32 vm_size, UINT32 vm_rss, UINT32 vm_swap)
No | > | **mmap2**(UINT64 addr, UINT64 length, FLAGS32 prot, FLAGS32 flags, FD fd, UINT64 pgoffset)
No | < | **mmap2**(UINT64 res, UINT32 vm_size, UINT32 vm_rss, UINT32 vm_swap)
No | > | **munmap**(UINT64 addr, UINT64 length)
No | < | **munmap**(ERRNO res, UINT32 vm_size, UINT32 vm_rss, UINT32 vm_swap)
No | > | **splice**(FD fd_in, FD fd_out, UINT64 size, FLAGS32 flags)
No | < | **splice**(ERRNO res)
Yes | > | **ptrace**(ENUMFLAGS16 request, PID pid)
Yes | < | **ptrace**(ERRNO res, DYNAMIC addr, DYNAMIC data)
Yes | > | **ioctl**(FD fd, UINT64 request, UINT64 argument)
Yes | < | **ioctl**(ERRNO res)
Yes | > | **rename**()
Yes | < | **rename**(ERRNO res, FSPATH oldpath, FSPATH newpath)
Yes | > | **renameat**()
Yes | < | **renameat**(ERRNO res, FD olddirfd, FSRELPATH oldpath, FD newdirfd, FSRELPATH newpath)
Yes | > | **symlink**()
Yes | < | **symlink**(ERRNO res, CHARBUF target, FSPATH linkpath)
Yes | > | **symlinkat**()
Yes | < | **symlinkat**(ERRNO res, CHARBUF target, FD linkdirfd, FSRELPATH linkpath)
Yes | > | **procexit**(ERRNO status, ERRNO ret, SIGTYPE sig, UINT8 core)
No | > | **sendfile**(FD out_fd, FD in_fd, UINT64 offset, UINT64 size)
No | < | **sendfile**(ERRNO res, UINT64 offset)
Yes | > | **quotactl**(FLAGS16 cmd, FLAGS8 type, UINT32 id, FLAGS8 quota_fmt)
Yes | < | **quotactl**(ERRNO res, CHARBUF special, CHARBUF quotafilepath, UINT64 dqb_bhardlimit, UINT64 dqb_bsoftlimit, UINT64 dqb_curspace, UINT64 dqb_ihardlimit, UINT64 dqb_isoftlimit, RELTIME dqb_btime, RELTIME dqb_itime, RELTIME dqi_bgrace, RELTIME dqi_igrace, FLAGS8 dqi_flags, FLAGS8 quota_fmt_out)
Yes | > | **setresuid**(UID ruid, UID euid, UID suid)
Yes | < | **setresuid**(ERRNO res)
Yes | > | **setresgid**(GID rgid, GID egid, GID sgid)
Yes | < | **setresgid**(ERRNO res)
Yes | > | **scapevent**(UINT32 event_type, UINT64 event_data)
Yes | > | **setuid**(UID uid)
Yes | < | **setuid**(ERRNO res)
Yes | > | **setgid**(GID gid)
Yes | < | **setgid**(ERRNO res)
No | > | **getuid**()
No | < | **getuid**(UID uid)
No | > | **geteuid**()
No | < | **geteuid**(UID euid)
No | > | **getgid**()
No | < | **getgid**(GID gid)
No | > | **getegid**()
No | < | **getegid**(GID egid)
No | > | **getresuid**()
No | < | **getresuid**(ERRNO res, UID ruid, UID euid, UID suid)
No | > | **getresgid**()
No | < | **getresgid**(ERRNO res, GID rgid, GID egid, GID sgid)
Yes | > | **clone**()
Yes | < | **clone**(PID res, CHARBUF exe, BYTEBUF args, PID tid, PID pid, PID ptid, CHARBUF cwd, INT64 fdlimit, UINT64 pgft_maj, UINT64 pgft_min, UINT32 vm_size, UINT32 vm_rss, UINT32 vm_swap, CHARBUF comm, BYTEBUF cgroups, FLAGS32 flags, UINT32 uid, UINT32 gid, PID vtid, PID vpid, UINT64 pidns_init_start_ts)
Yes | > | **fork**()
Yes | < | **fork**(PID res, CHARBUF exe, BYTEBUF args, PID tid, PID pid, PID ptid, CHARBUF cwd, INT64 fdlimit, UINT64 pgft_maj, UINT64 pgft_min, UINT32 vm_size, UINT32 vm_rss, UINT32 vm_swap, CHARBUF comm, BYTEBUF cgroups, FLAGS32 flags, UINT32 uid, UINT32 gid, PID vtid, PID vpid, UINT64 pidns_init_start_ts)
Yes | > | **vfork**()
Yes | < | **vfork**(PID res, CHARBUF exe, BYTEBUF args, PID tid, PID pid, PID ptid, CHARBUF cwd, INT64 fdlimit, UINT64 pgft_maj, UINT64 pgft_min, UINT32 vm_size, UINT32 vm_rss, UINT32 vm_swap, CHARBUF comm, BYTEBUF cgroups, FLAGS32 flags, UINT32 uid, UINT32 gid, PID vtid, PID vpid, UINT64 pidns_init_start_ts)
No | > | **signaldeliver**(PID spid, PID dpid, SIGTYPE sig)
Yes | > | **procinfo**(UINT64 cpu_usr, UINT64 cpu_sys)
No | > | **getdents**(FD fd)
No | < | **getdents**(ERRNO res)
No | > | **getdents64**(FD fd)
No | < | **getdents64**(ERRNO res)
Yes | > | **setns**(FD fd, FLAGS32 nstype)
Yes | < | **setns**(ERRNO res)
Yes | > | **flock**(FD fd, FLAGS32 operation)
Yes | < | **flock**(ERRNO res)
Yes | > | **cpu_hotplug**(UINT32 cpu, UINT32 action)
Yes | > | **accept**()
Yes | < | **accept**(FD fd, SOCKTUPLE tuple, UINT8 queuepct, UINT32 queuelen, UINT32 queuemax)
Yes | > | **accept**(INT32 flags)
Yes | < | **accept**(FD fd, SOCKTUPLE tuple, UINT8 queuepct, UINT32 queuelen, UINT32 queuemax)
No | > | **semop**(INT32 semid)
No | < | **semop**(ERRNO res, UINT32 nsops, UINT16 sem_num_0, INT16 sem_op_0, FLAGS16 sem_flg_0, UINT16 sem_num_1, INT16 sem_op_1, FLAGS16 sem_flg_1)
No | > | **semctl**(INT32 semid, INT32 semnum, FLAGS16 cmd, INT32 val)
No | < | **semctl**(ERRNO res)
No | > | **ppoll**(FDLIST fds, RELTIME timeout, SIGSET sigmask)
No | < | **ppoll**(ERRNO res, FDLIST fds)
Yes | > | **mount**(FLAGS32 flags)
Yes | < | **mount**(ERRNO res, CHARBUF dev, FSPATH dir, CHARBUF type)
Yes | > | **umount**(FLAGS32 flags)
Yes | < | **umount**(ERRNO res, FSPATH name)
Yes | > | **k8s**(CHARBUF json)
No | > | **semget**(INT32 key, INT32 nsems, FLAGS32 semflg)
No | < | **semget**(ERRNO res)
No | > | **access**(FLAGS32 mode)
No | < | **access**(ERRNO res, FSPATH name)
Yes | > | **chroot**()
Yes | < | **chroot**(ERRNO res, FSPATH path)
Yes | > | **tracer**(INT64 id, CHARBUFARRAY tags, CHARBUF_PAIR_ARRAY args)
Yes | < | **tracer**(INT64 id, CHARBUFARRAY tags, CHARBUF_PAIR_ARRAY args)
Yes | > | **mesos**(CHARBUF json)
Yes | > | **setsid**()
Yes | < | **setsid**(PID res)
Yes | > | **mkdir**(UINT32 mode)
Yes | < | **mkdir**(ERRNO res, FSPATH path)
Yes | > | **rmdir**()
Yes | < | **rmdir**(ERRNO res, FSPATH path)
Yes | > | **notification**(CHARBUF id, CHARBUF desc)
Yes | > | **unshare**(FLAGS32 flags)
Yes | < | **unshare**(ERRNO res)
Yes | > | **infra**(CHARBUF source, CHARBUF name, CHARBUF description, CHARBUF scope)
No | > | **page_fault**(UINT64 addr, UINT64 ip, FLAGS32 error)
Yes | > | **execve**(FSPATH filename)
Yes | < | **execve**(ERRNO res, CHARBUF exe, BYTEBUF args, PID tid, PID pid, PID ptid, CHARBUF cwd, UINT64 fdlimit, UINT64 pgft_maj, UINT64 pgft_min, UINT32 vm_size, UINT32 vm_rss, UINT32 vm_swap, CHARBUF comm, BYTEBUF cgroups, BYTEBUF env, INT32 tty, PID pgid, INT32 loginuid, FLAGS32 flags, UINT64 cap_inheritable, UINT64 cap_permitted, UINT64 cap_effective, UINT64 exe_ino, ABSTIME exe_ino_ctime, ABSTIME exe_ino_mtime)
Yes | > | **setpgid**(PID pid, PID pgid)
Yes | < | **setpgid**(PID res)
Yes | > | **seccomp**(UINT64 op)
Yes | < | **seccomp**(ERRNO res)
Yes | > | **unlink**()
Yes | < | **unlink**(ERRNO res, FSPATH path)
Yes | > | **unlinkat**()
Yes | < | **unlinkat**(ERRNO res, FD dirfd, FSRELPATH name, FLAGS32 flags)
Yes | > | **mkdirat**()
Yes | < | **mkdirat**(ERRNO res, FD dirfd, FSRELPATH path, UINT32 mode)
Yes | > | **openat**(FD dirfd, FSRELPATH name, FLAGS32 flags, UINT32 mode)
Yes | < | **openat**(FD fd, FD dirfd, FSRELPATH name, FLAGS32 flags, UINT32 mode, UINT32 dev, UINT64 ino)
Yes | > | **link**()
Yes | < | **link**(ERRNO res, FSPATH oldpath, FSPATH newpath)
Yes | > | **linkat**()
Yes | < | **linkat**(ERRNO res, FD olddir, FSRELPATH oldpath, FD newdir, FSRELPATH newpath, FLAGS32 flags)
Yes | > | **fchmodat**()
Yes | < | **fchmodat**(ERRNO res, FD dirfd, FSRELPATH filename, MODE mode)
Yes | > | **chmod**()
Yes | < | **chmod**(ERRNO res, FSPATH filename, MODE mode)
Yes | > | **fchmod**()
Yes | < | **fchmod**(ERRNO res, FD fd, MODE mode)
Yes | > | **renameat2**()
Yes | < | **renameat2**(ERRNO res, FD olddirfd, FSRELPATH oldpath, FD newdirfd, FSRELPATH newpath, FLAGS32 flags)
Yes | > | **userfaultfd**()
Yes | < | **userfaultfd**(ERRNO res, FLAGS32 flags)
No | > | **pluginevent**(UINT32 plugin ID, BYTEBUF event_data)
Yes | > | **container**(CHARBUF json)
Yes | > | **openat2**(FD dirfd, FSRELPATH name, FLAGS32 flags, UINT32 mode, FLAGS32 resolve)
Yes | < | **openat2**(FD fd, FD dirfd, FSRELPATH name, FLAGS32 flags, UINT32 mode, FLAGS32 resolve)
No | > | **mprotect**(UINT64 addr, UINT64 length, FLAGS32 prot)
No | < | **mprotect**(ERRNO res)
Yes | > | **execveat**(FD dirfd, FSRELPATH pathname, FLAGS32 flags)
Yes | < | **execveat**(ERRNO res, CHARBUF exe, BYTEBUF args, PID tid, PID pid, PID ptid, CHARBUF cwd, UINT64 fdlimit, UINT64 pgft_maj, UINT64 pgft_min, UINT32 vm_size, UINT32 vm_rss, UINT32 vm_swap, CHARBUF comm, BYTEBUF cgroups, BYTEBUF env, INT32 tty, PID pgid, INT32 loginuid, FLAGS32 flags, UINT64 cap_inheritable, UINT64 cap_permitted, UINT64 cap_effective, UINT64 exe_ino, ABSTIME exe_ino_ctime, ABSTIME exe_ino_mtime)
No | > | **copy_file_range**(FD fdin, UINT64 offin, UINT64 len)
No | < | **copy_file_range**(ERRNO res, FD fdout, UINT64 offout)
Yes | > | **clone3**()
Yes | < | **clone3**(PID res, CHARBUF exe, BYTEBUF args, PID tid, PID pid, PID ptid, CHARBUF cwd, INT64 fdlimit, UINT64 pgft_maj, UINT64 pgft_min, UINT32 vm_size, UINT32 vm_rss, UINT32 vm_swap, CHARBUF comm, BYTEBUF cgroups, FLAGS32 flags, UINT32 uid, UINT32 gid, PID vtid, PID vpid, UINT64 pidns_init_start_ts)
Yes | > | **open_by_handle_at**()
Yes | < | **open_by_handle_at**(FD fd, FD mountfd, FLAGS32 flags, FSPATH path)
Yes | > | **io_uring_setup**()
Yes | < | **io_uring_setup**(ERRNO res, UINT32 entries, UINT32 sq_entries, UINT32 cq_entries, FLAGS32 flags, UINT32 sq_thread_cpu, UINT32 sq_thread_idle, FLAGS32 features)
No | > | **io_uring_enter**()
No | < | **io_uring_enter**(ERRNO res, FD fd, UINT32 to_submit, UINT32 min_complete, FLAGS32 flags, SIGSET sig)
No | > | **io_uring_register**()
No | < | **io_uring_register**(ERRNO res, FD fd, ENUMFLAGS16 opcode, UINT64 arg, UINT32 nr_args)
No | > | **mlock**()
No | < | **mlock**(ERRNO res, UINT64 addr, UINT64 len)
No | > | **munlock**()
No | < | **munlock**(ERRNO res, UINT64 addr, UINT64 len)
No | > | **mlockall**()
No | < | **mlockall**(ERRNO res, FLAGS32 flags)
No | > | **munlockall**()
No | < | **munlockall**(ERRNO res)
Yes | > | **capset**()
Yes | < | **capset**(ERRNO res, UINT64 cap_inheritable, UINT64 cap_permitted, UINT64 cap_effective)
Yes | > | **useradded**(UINT32 uid, UINT32 gid, CHARBUF name, CHARBUF home, CHARBUF shell, CHARBUF container_id)
Yes | > | **userdeleted**(UINT32 uid, UINT32 gid, CHARBUF name, CHARBUF home, CHARBUF shell, CHARBUF container_id)
Yes | > | **groupadded**(UINT32 gid, CHARBUF name, CHARBUF container_id)
Yes | > | **groupdeleted**(UINT32 gid, CHARBUF name, CHARBUF container_id)
Yes | > | **dup2**(FD fd)
Yes | < | **dup2**(FD res, FD oldfd, FD newfd)
Yes | > | **dup3**(FD fd)
Yes | < | **dup3**(FD res, FD oldfd, FD newfd, FLAGS32 flags)
Yes | > | **dup**(FD fd)
Yes | < | **dup**(FD res, FD oldfd)
Yes | > | **bpf**(INT64 cmd)
Yes | < | **bpf**(FD fd)
No | > | **mlock2**()
No | < | **mlock2**(ERRNO res, UINT64 addr, UINT64 len, UINT32 flags)
No | > | **fsconfig**()
No | < | **fsconfig**(ERRNO res, FD fd, ENUMFLAGS32 cmd, CHARBUF key, BYTEBUF value_bytebuf, CHARBUF value_charbuf, INT32 aux)
Yes | > | **epoll_create**(INT32 size)
Yes | < | **epoll_create**(ERRNO res)
Yes | > | **epoll_create1**(FLAGS32 flags)
Yes | < | **epoll_create1**(ERRNO res)
