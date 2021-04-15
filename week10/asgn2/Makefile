#Please modify the following two fields to contain your id number and your
#surname. You can place spaces in your surname if you need to.
ID = 12345
SURNAME = MacGyver

#DO NOT MODIFY ANYTHING BEYOND THIS POINT: YOU RISK LOSING YOUR WORK!

ASGN_NO = 2
SUBMIT_DIR = "${SURNAME}"_${ID}_A${ASGN_NO}
SUBMIT_TAR = ${SUBMIT_DIR}.tar
SUBMIT_FILE = ${SUBMIT_DIR}.tar.gz

%default: submission
%phony: submission clean

submission:
	@echo -e '\n\n----{ Making submission tree }----'
	mkdir -p ${SUBMIT_DIR}
	cp chain.l ${SUBMIT_DIR}/.
	cp chain.y ${SUBMIT_DIR}/.
	cp -r problem? ${SUBMIT_DIR}
	tar -cvf ${SUBMIT_TAR} ${SUBMIT_DIR}
	gzip ${SUBMIT_TAR}
	@echo -e '----{ Submission archive ready }----\n\n'
clean:
	@echo -e '\n\n----{ Tidying up submission tree }----'
	rm -f ${SUBMIT_DIR}/problem?/.[!.]*
	rm -f ${SUBMIT_DIR}/problem?/*
	rmdir ${SUBMIT_DIR}/problem?
	rm -f ${SUBMIT_DIR}/.[!.]*
	rm -f ${SUBMIT_DIR}/*
	rmdir ${SUBMIT_DIR}
	rm -f ${SUBMIT_FILE}
	@echo -e '----{ Submission archive removed }----\n\n'
