
# NAME 

     bsdiff -- generate a patch between two binary files

# SYNOPSIS
```
   bsdiff oldfile newfile patchfile
```
# DESCRIPTION
  
	   The bsdiff utility compares oldfile to newfile and writes to patchfile a
     binary patch suitable for use by bspatch(1).  When oldfile and newfile
     are two versions of an executable program, the patches produced are on
     average a factor of five smaller than those produced by any other binary
     patch tool known to the author.

     The bsdiff utility uses memory equal to 17 times the size of oldfile, and
     requires an absolute minimum working set size of 8 times the size of
     oldfile.

# SEE ALSO 

     bspatch(1)

# AUTHORS

     Colin Percival <cperciva@FreeBSD.org>

# BUGS

     The bsdiff utility does not store the hashes of oldfile or newfile in
     patchfile.  As a result, it is possible to apply a patch to the wrong
     file; this will usually produce garbage.  It is recommended that users of
     bsdiff store the hashes of oldfile and newfile and compare against them
     before and after applying patchfile.

FreeBSD 9.0                      May 18, 2003                      FreeBSD 9.0

