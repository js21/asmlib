AR = ar
RANLIB = ranlib

.asm.o64:
	yasm -felf64 -DUNIX -o $*.o64 $<

.SUFFIXES: .asm .o64


AELF64_OBJS = instrset64.o64 procname64.o64 \
cpuid64.o64 rdtsc64.o64 round64.o64 \
memcpy64.o64 memmove64.o64 memset64.o64 memcmp64.o64 \
strlen64.o64 strcpy64.o64 strcat64.o64 \
strstr64.o64 strcmp64.o64 stricmp64.o64 \
strtouplow64.o64 substring64.o64 strspn64.o64 \
strcountutf864.o64 strcountset64.o64 \
divfixedi64.o64 divfixedv64.o64 popcount64.o64 \
physseed64.o64 mother64.o64 mersenne64.o64 \
sfmt64.o64 \
cputype64.o64 debugbreak64.o64 unalignedisfaster64.o64 \
cachesize64.o64

libaelf64.a: $(AELF64_OBJS)
	$(AR) -rc $@ $(AELF64_OBJS)
	-$(RANLIB) $@
