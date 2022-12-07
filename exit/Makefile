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
