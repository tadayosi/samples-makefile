define echo1
	echo $(1) && sleep 0.01
endef

loop1:
	@for i in {1..100}; do \
		$(call echo1,$$i); \
	done

define echo2
	(echo $(1) && sleep 0.01)
endef

loop2:
	@for i in {1..100}; do \
		$(call echo2,$$i); \
	done

loop-cd1:
	@mkdir -p {1..3}
	@for i in {1..3}; do \
		#cd $$i; pwd; # error! \
		(cd $$i; pwd); \
	done
	@rmdir {1..3}

define cd2
	(cd $(1); pwd)
endef

loop-cd2:
	@mkdir -p {1..3}
	@for i in {1..3}; do \
		$(call cd2,$$i); \
	done
	@rmdir {1..3}

cd:
	@mkdir -p {1..3}
	@cd 1; pwd
	@cd 2; pwd
	@cd 3; pwd
	@rmdir {1..3}
