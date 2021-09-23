DragonFly belongs to the same class of operating systems as other BSD-derived
systems and Linux.
It is based on the same UNIX ideals and APIs and shares ancestor code with other
BSD operating systems.
DragonFly provides an opportunity for the BSD base to grow in an entirely
different direction from the one taken in the FreeBSD, NetBSD, and OpenBSD
series.

DragonFly includes many useful features that differentiate it from other
operating systems in the same class.

The most prominent one is HAMMER, our modern high performance filesystem with
built-in mirroring and historic access functionality.

Virtual kernels provide the ability to run a full-blown kernel as a user process
for the purpose of managing resources or for accelerated kernel development and
debugging.

The kernel uses several synchronization and locking mechanisms for SMP.
Much of the work done since the project began has been in this area.
A combination of intentional simplification of certain classes of locks to make
more expansive subsystems less prone to deadlocks, and the rewriting of nearly
all the original codebase using algorithms designed specifically with SMP in
mind, has resulted in an extremely stable, high-performance kernel that is
capable of efficiently using all cpu, memory, and I/O resources thrown at it.

DragonFlyBSD has virtually no bottlenecks or lock contention in-kernel.
Nearly all operations are able to run concurrently on any number of cpus.
Over the years, the VFS support infrastructure (namecache, vnode cache), user
support infrastructure (uid, gid, process groups, sessions), process and
threading infrastructure, storage subsystems, networking, user and kernel memory
allocation and management, process fork, exec, and exit/teardown, time keeping,
and all other aspects of kernel design have been rewritten with extreme SMP
performance as a goal.

DragonFly is uniquely positioned to take advantage of the wide availability of
affordable Solid Storage Devices (SSDs), by making use of swap space to cache
filesystem data and meta-data.
This feature, commonly referred to as "swapcache", can give a significant boost
to both server and workstation workloads, with a very minor hardware investment.

The DragonFly storage stack comprises robust, natively written AHCI and NVME
drivers, stable device names via DEVFS and a partial implementation of Device
Mapper for reliable volume management and encryption.

Some other features that are especially useful to system administrators are a
performant and scalable TMPFS implementation, an extremely efficient NULLFS that
requires no internal replication of directory or file vnodes, our natively
written DNTPD (ntp client) which uses full-bore line intercept and standard
deviation summation for highly-accurate timekeeping, and DMA, designed to
provide low-overhead email services for system operators who do not need more
expansive mail services such as postfix or sendmail.

A major crux of any open source operating system is third party applications.
DragonFly leverages the dports system to provide thousands of applications in
source and binary forms.
These features and more band together to make DragonFly a modern, useful,
friendly and familiar UNIX-like operating system.

The DragonFly BSD community is made up of users and developers that take pride
in an operating system that maintains challenging goals and ideals.
This community has no reservation about cutting ties with legacy when it makes
sense, preferring a pragmatic, no-nonsense approach to development of the
system.
The community also takes pride in its openness and innovative spirit,
applying patience liberally and always trying to find a means to meet or
exceed the performance of our competitors while maintaining our trademark
algorithmic simplicity.

