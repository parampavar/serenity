OBJS = \
    AboutDialog.o \
    AbstractButton.o \
    AbstractTableView.o \
    AbstractView.o \
    Action.o \
    ActionGroup.o \
    Application.o \
    BoxLayout.o \
    Button.o \
    CheckBox.o \
    Clipboard.o \
    ColorInput.o \
    ColorPicker.o \
    ColumnsView.o \
    ComboBox.o \
    Command.o \
    CppLexer.o \
    CppSyntaxHighlighter.o \
    Desktop.o \
    Dialog.o \
    DisplayLink.o \
    DragOperation.o \
    Event.o \
    FilePicker.o \
    FileSystemModel.o \
    FontDatabase.o \
    Frame.o \
    GroupBox.o \
    Icon.o \
    IconView.o \
    InputBox.o \
    INILexer.o \
    INISyntaxHighlighter.o \
    JsonArrayModel.o \
    JSSyntaxHighlighter.o \
    Label.o \
    Layout.o \
    LazyWidget.o \
    ListView.o \
    Menu.o \
    MenuBar.o \
    MenuItem.o \
    MessageBox.o \
    Model.o \
    ModelIndex.o \
    ModelSelection.o \
    MultiView.o \
    Notification.o \
    Painter.o \
    ProgressBar.o \
    RadioButton.o \
    ResizeCorner.o \
    ScrollBar.o \
    ScrollableWidget.o \
    Shortcut.o \
    Slider.o \
    SortingProxyModel.o \
    SpinBox.o \
    Splitter.o \
    StackWidget.o \
    StatusBar.o \
    SyntaxHighlighter.o \
    TabWidget.o \
    TableView.o \
    TextBox.o \
    TextDocument.o \
    TextEditor.o \
    ToolBar.o \
    ToolBarContainer.o \
    TreeView.o \
    UndoStack.o \
    Variant.o \
    Widget.o \
    Window.o \
    WindowServerConnection.o

LIBRARY = libgui.a

Application.cpp: ../../Services/WindowServer/WindowServerEndpoint.h

../../Services/WindowServer/WindowServerEndpoint.h:
	@flock $(dir $(@)) $(MAKE) -C $(dir $(@))

# HACK: NotificationServer depends on LibGUI so we don't flock for these..
Notification.cpp: ../../Services/NotificationServer/NotificationServerEndpoint.h ../../Services/NotificationServer/NotificationClientEndpoint.h

../../Services/NotificationServer/NotificationServerEndpoint.h:
	$(MAKE) -C $(dir $(@)) NotificationServerEndpoint.h

../../Services/NotificationServer/NotificationClientEndpoint.h:
	$(MAKE) -C $(dir $(@)) NotificationClientEndpoint.h

install:
	mkdir -p $(SERENITY_BASE_DIR)/Root/usr/include/LibGUI/
	cp ./*.h $(SERENITY_BASE_DIR)/Root/usr/include/LibGUI/
	cp $(LIBRARY) $(SERENITY_BASE_DIR)/Root/usr/lib/

include ../../Makefile.common
