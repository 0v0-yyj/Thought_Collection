``` Octave
degree = #;
out = ones(size(X(:,1))); % keeps row number, sample #
for i = 1:degree
    for j = 0:i
      %按照次方产生feature, 从零次方到六次方, 逐渐增加
        out(:, end+1) = (X1.^(i-j)).*(X2.^j);
    end
end

end
```

* i= 1
    * j = 0, x1; j= 1, x2
* i = 2
    * j = 0, x1^2; j = 1, x1*x2; j = 2, x2^2
* i = 3
    * j = 0, x1^3; j = 1, x1^2*x2^1; j = 2, x1^1*x2^2; j = 3, x2^3                      
    
......
