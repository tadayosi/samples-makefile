test1:
	FAILED=0; \
	./test.sh 0 || FAILED=1; \
	./test.sh 1 || FAILED=1; \
	./test.sh 0 || FAILED=1; \
	exit $${FAILED}

test2:
	FAILED=0; \
	./test.sh 0 || FAILED=1; \
	./test.sh 0 || FAILED=1; \
	./test.sh 0 || FAILED=1; \
	exit $${FAILED}

test3:
	./test.sh 0 && \
	./test.sh 1 && \
	./test.sh 0

test4:
	A=0; B=0; C=0; \
	./test.sh 1 || A=1; \
	./test.sh 1 || B=1; \
	./test.sh 1 || C=1; \
	echo $${A} $${B} $${C}

test5:
	@echo 1
	@(echo 2; exit 1; echo 3)
	@echo 4

test51:
	@echo 1
	@echo 2; ./test.sh 1; echo 3
	@echo 4

test52:
	@echo 1
	@(echo 2; ./test.sh 1; echo 3)
	@echo 4

test53:
	@echo 1
	@echo 2 && ./test.sh 1 && echo 3
	@echo 4

test54:
	@echo 1
	@(echo 2 && ./test.sh 1 && echo 3)
	@echo 4

define call6
	@(echo $(1); ./test.sh 1; echo $(2))
endef

test6:
	@echo 1
	@$(call call6,2,3)
	@echo 4

define call61
	@(echo $(1) && ./test.sh 1 && echo $(2))
endef

test61:
	@echo 1
	@$(call call61,2,3)
	@echo 4
