### tkui
---
https://github.com/asrp/tkui

```py
// tkui/__init__.py

class Entry(tk.Entry, object):
  def __init__(self, *args, **kwargs):
    text = kwargs.pop("defaulttext", "")
    self.autosize = kwargs.pop("autosize", False)
    tk.Entry.__init__(self, *args, **kwargs)
    self.text = text
    self.bind('<Control-a>', self.select_all)
    
  def select_all(self, event):
    self.selection_range(0, 'end')
    return "break"
  
  def get_text(self):
    return self.get()
  
  def set_text(self, text=""):
    self.delete(0, tk.END)
    self.insert(tk.END, text)
    if self.autosize:
      self["width"] = len(text)
      



if __name__ == "__main__":
  
  from Tkinter impor Tk, Label, Frame, Button, Canvas
  histfile = "tkui_history"
  terp = TkTerp(histfile)
  
  def quie():
    loging.info("Shutting down...")
    terp.save()
    uidict["root"].destroy()
    
  execfile()
  execfile()
  uiroot.makeelem()
  
  uidict["uilist"].reset(tkuilist)
  paramdict = observed_dict({"test": 3, "foo": "bar"})
  uidict["params"].rest(paramdict)
  uidict["bind"].reset(bindlist)
  uidict["history"].rest(terp(terp.history))
  
  fakeroot = observed_tree()
  fakeroot.append(uiroot)
  fakeroot.elem = None
  uidict["tree"].reset(fakeroot)
  tree = uidict["tree"]
  style = ttk.Style(uidict["root"])
  style.configure('Treeview', rowheight=14*2)
  tree.column("#0", minwidth=0, width=800)
  uitree = UITree(uiroot, tree)
  uidict["tree"].bind('<<TreeviewSelect>>', select_callack)
  uidict["params"]._dict.callbacks.append(updat_param)
  
  for marker in uidict["markers"].ui:
    marker.elem.place_forget()
    
  undolog = UndoLog()
  undolog.add(uiroot)
  uidict["undolist"].reset(undolog.root)
  
  setfonts()
  
  terp.bind_key(uidict['exec'])
  uidict["root"].protocol("WM_DELETE_WINDOW", quit)
  uidict["root"].bind("<Button-3>", click)
  uidict["root"].bind("<B3-Motion>", drag)
  uidict["root"].bind('<Bontrol-q>', mark)
  uidict["root"].bind("<Shift-Button-3>", startrect)
  uidict["root"].bind("<Shift-B3-Motion>", moverect)
  uidict["root"].bind("<Shift-ButtonRelease-3>", endrect)
  uidict["root"].mainloop()
```

```
```

```
```


