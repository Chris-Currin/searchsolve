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

Q: git stop monitoring changes for a file

A: 
```bash
> git update-index --assume-unchanged <file>
```
Note that this is non-recursive for folders (as of 2018-04). 

To undo use `--no-assume-unchanged`

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

Q: Publication quality figures:

A: http://dgleich.github.io/hq-matlab-figs/

alt: http://asa.scitation.org/pb-assets/files/publications/jas/figures.pdf

```MATLAB
% The new defaults will not take effect if there are any open figures. To
% use them, we close all figures, and then repeat the first example.
close all;

% The properties we've been using in the figures
set(0,'defaultLineLineWidth',lw);   % set the default line width to lw
set(0,'defaultLineMarkerSize',msz); % set the default line marker size to msz
set(0,'defaultLineLineWidth',lw);   % set the default line width to lw
set(0,'defaultLineMarkerSize',msz); % set the default line marker size to msz

% Set the default Size for display
defpos = get(0,'defaultFigurePosition');
set(0,'defaultFigurePosition', [defpos(1) defpos(2) width*100, height*100]);

% Set the defaults for saving/printing to a file
set(0,'defaultFigureInvertHardcopy','on'); % This is the default anyway
set(0,'defaultFigurePaperUnits','inches'); % This is the default anyway
defsize = get(gcf, 'PaperSize');
left = (defsize(1)- width)/2;
bottom = (defsize(2)- height)/2;
defsize = [left, bottom, width, height];
set(0, 'defaultFigurePaperPosition', defsize);

% Now we repeat the first example but do not need to include anything
% special beyond manually specifying the tick marks.
figure(1); clf;
plot(dmn,f(dmn),'b-',dmn,g(dmn),'r--',xeq,f(xeq),'g*');
xlim([-pi pi]);
legend('f(x)', 'g(x)', 'f(x)=g(x)', 'Location', 'SouthEast');
xlabel('x');
title('Automatic Example Figure');
set(gca,'XTick',-3:3); %<- Still need to manually specific tick marks
set(gca,'YTick',0:10); %<- Still need to manually specific tick marks
```

## Linux

## Word
Q: Replace with subscript/superscript

A: https://word.tips.net/T003837_Replacing_with_a_Subscript

_In the Replace With box enter the characters ^c. This informs Word that you want to replace any instances of the Find What text with whatever is in the Clipboard (your properly formatted text)._

