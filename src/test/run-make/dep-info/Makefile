-include ../tools.mk
all:
	$(RUSTC) --dep-info --lib lib.rs
	sleep 1
	touch foo.rs
	-rm -f done
	$(MAKE) -f Makefile.foo
	rm done
	$(MAKE) -f Makefile.foo
	rm done && exit 1 || exit 0
