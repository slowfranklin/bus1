#
# By setting BUS1_EXT=X, the bus1 module will be built as busX.ko, and
# KBUILD_MODNAME=busX. This has the effect that all exported objects have
# different names than usual and you can run your test-infrastructure against
# the busX.ko, while running your system on bus1.ko.
#
# To just build the module, use:
#     make BUS1_EXT=2 M=ipc/bus1
#

bus$(BUS1_EXT)-y :=	\
	active.o	\
	handle.o	\
	main.o		\
	message.o	\
	peer.o		\
	pool.o		\
	queue.o		\
	transaction.o	\
	util.o		\
	user.o

bus$(BUS1_EXT)-$(CONFIG_BUS1_TESTS) += tests.o

obj-$(CONFIG_BUS1) += bus$(BUS1_EXT).o
