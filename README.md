# varonis
Varonis Homework


figure out how many passwords I can send before getting locked out or app crashes
I want to use a dictionary to pass every possible password of (a-z permutation) to application
Running the app only unlocks when you give it the correct password sending Success to STDOUT
not a website, no burp or things like that which become useless
Conclusion:
I want to read from a dictionary file or memory program to send subsequent lines to the password vault. Grep for "Success". Wrong password is output, move to the next line, sleep for (n)seconds and try again.

[vault.o_strings.txt](https://github.com/n2h-git/varonis/files/8511896/vault.o_strings.txt)

[vault_strings.txt](https://github.com/n2h-git/varonis/files/8511897/vault_strings.txt)



realized this is a side-channel timing attack after rereading the pdf.

researched side-channel attack and discovered https://github.com/mCodingLLC/VideosSampleCode/blob/master/videos/061_time_to_hack_cracking_passwords_using_timing_information_secure_python/timing_attack.py

find way to run that code or similar against the vault.o STDIN and check for increase (subtle or overt) in response timing

[bruteforce.txt](https://github.com/n2h-git/varonis/files/8511900/bruteforce.txt)

[bruteforce2.txt](https://github.com/n2h-git/varonis/files/8511902/bruteforce2.txt)


┌──(kali㉿kali)-[~/Varonis]
└─$ strings vault.o      
/lib64/ld-linux-x86-64.so.2
iL0Ok
__gmon_start__
libc.so.6
exit
strncpy
puts
printf
strlen
usleep
__libc_start_main
GLIBC_2.2.5
fff.
fffff.
l$ L
t$(L
|$0H
Enter the password as the first parameter/n
Wrong password
SUCCESS!
GCC: (GNU) 4.4.7 20120313 (Red Hat 4.4.7-11)
GCC: (GNU) 4.4.7 20120313 (Red Hat 4.4.7-17)
.symtab
.strtab
.shstrtab
.interp
.note.ABI-tag
.note.gnu.build-id
.gnu.hash
.dynsym
.dynstr
.gnu.version
.gnu.version_r
.rela.dyn
.rela.plt
.init
.text
.fini
.rodata
.eh_frame_hdr
.eh_frame
.ctors
.dtors
.jcr
.dynamic
.got
.got.plt
.data
.bss
.comment
call_gmon_start
crtstuff.c
__CTOR_LIST__
__DTOR_LIST__
__JCR_LIST__
__do_global_dtors_aux
completed.6352
dtor_idx.6354
frame_dummy
__CTOR_END__
__FRAME_END__
__JCR_END__
__do_global_ctors_aux
ta_Medium.c
_GLOBAL_OFFSET_TABLE_
__init_array_end
__init_array_start
_DYNAMIC
data_start
printf@@GLIBC_2.2.5
__libc_csu_fini
_start
__gmon_start__
_Jv_RegisterClasses
puts@@GLIBC_2.2.5
exit@@GLIBC_2.2.5
_fini
__libc_start_main@@GLIBC_2.2.5
_IO_stdin_used
strlen@@GLIBC_2.2.5
__data_start
usleep@@GLIBC_2.2.5
__dso_handle
__DTOR_END__
__libc_csu_init
__bss_start
_end
strncpy@@GLIBC_2.2.5
_edata
main
_init
