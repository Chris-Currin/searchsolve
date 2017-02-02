# What I have searched and the (potential) solutions


## Git
? git undo stage changes

```bash
> git reset [filename|folder]
```

```bash
> git rm -r -f [filename|folder]
```
removes from disk too

## MATLAB
Set image at A4 page size:
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
