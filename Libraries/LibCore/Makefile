OBJS = \
    ArgsParser.o \
    ConfigFile.o \
    DateTime.o \
    DirIterator.o \
    ElapsedTimer.o \
    Event.o \
    EventLoop.o \
    File.o \
    Gzip.o \
    IODevice.o \
    LocalServer.o \
    LocalSocket.o \
    MimeData.o \
    NetworkJob.o \
    NetworkResponse.o \
    Notifier.o \
    Object.o \
    ProcessStatisticsReader.o \
    Socket.o \
    SocketAddress.o \
    StandardPaths.o \
    TCPServer.o \
    TCPSocket.o \
    Timer.o \
    UDPServer.o \
    UDPSocket.o \
    puff.o

LIBRARY = libcore.a

install:
	mkdir -p $(SERENITY_BASE_DIR)/Root/usr/include/LibCore/
	cp *.h $(SERENITY_BASE_DIR)/Root/usr/include/LibCore/
	cp $(LIBRARY) $(SERENITY_BASE_DIR)/Root/usr/lib/

include ../../Makefile.common
