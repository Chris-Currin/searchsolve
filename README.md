# What I have searched and the (potential) solutions


## Git
Q: git undo stage changes

A: 
```bash
> git reset [filename|folder]
```

```bash
> git rm -r -f [filename|folder]
```
removes from disk too

## MATLAB
Q: Set image as A4 page size:

A: 
```matlab
set(fig, 'Units', 'Inches', 'Position', [0,0,8.27,11.69],...
    'PaperUnits', 'Inches', 'PaperSize', [8.27,11.69])
```

Change the scale of the image: 
```matlab
scale = [1,0.5]
...,'Position',[[0,0],scale.*[8.27,11.69]],...
```

## Linux
