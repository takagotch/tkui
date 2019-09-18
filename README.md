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
      
      
```

```
```

```
```


