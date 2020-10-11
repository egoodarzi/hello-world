fomat long -->
format short
save filename
save filename variable
load filename
load filename variable
4-1:
Manually Entering Arrays:
x = [1 2 3] or x = [1, 2, 3] creates row vector
x = [1; 2; 3] creates column vector
space or comma for row vector
semicolumn for column vector
	matlab stands for MATrix LABoratory
4-2:
creating Evenly-spaced Vectors
	x = [2:10]
	x = [1:2:10]
	x = (1:2:10)
	x = linspace(1,10,100)
4-3:
x = rand(5)
x = rand(5,1)
x = zeros(6,3)
x = zeros(6,3)
rand(size(x))
5-1 Indexing into Arrays
A(1) -->  in a 2D array counts down from first column and goes to next column and continues.
A(1,2) row 1 and column 2
A(1,:) row 1 all elements
5-2 Extracting multiple Elements
x = v(3:end)
density([1,3,6])
6-1 Performing array operations on vectors
max(x)
sqrt(x)
round(x)
matrix multiplation --> 		*
elementwise multiplication --> 		.*
7-1 Obtaining Multiple Outputs from function calls
size(x)
[dr , dc] = size(data)
[~, imax] = max(vector)
**you can use matlab help
8-1
randi(iMax, rows, columns)
doc randi
9-1 Plotting Vectors
plot(x,y)
plot(x,y,'r--*')
hold 0n
hold off
plot(v1, 'LineWidth', 3)
plot(x,y,"ro-","LineWidth",5)
histogram(density, 'FaceColor', 'y')
9-2 Annotating Plots
Labels can be added to plots using plot annotation functions, such as title. The input to these functions is a string. Strings in MATLAB are enclosed in double quotes (").
plot(x, y, "ks")
title("Plot title")
ylabel("Mass (g)")
legend("a", "b", "c")
bar(data(3, :))   --> bar plot
xlim([0 1000])

12- Logical Arrays
> < ==  ~=
test  = 2 < 4     ---> reault is 0 or 1
v = v1(v1 < 4)   ---> use logical array as index
v1(v1 < 4) = 0
x = v1(v1>6 | v1<2)
x = v1(v1<4 & v1>2)
13-1
if x>0
	then do that
elseif
else
end
--
for x = 1:5
	do that 
end

for idx = 1:length(density)
pause(0.2)
14-1 Project Stellar Motion
