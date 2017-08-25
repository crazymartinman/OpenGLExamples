## Win32 OpenGL Boilerplate

### OpenGL Functions:

#### glViewPort
````
glViewport — set the viewport
````

***C Specification:***
````C
void glViewport(GLint x, GLint y, GLsizei width, GLsizei height);
````

***Parameters***
````
x, y
Specify the lower left corner of the viewport rectangle, in pixels. The initial value is ( 0 , 0 ).

width, height
Specify the width and height of the viewport. When a GL context is first attached to a window, width and height are set to the dimensions of that window.

````

***Description:***
````
glViewport specifies the affine transformation of x and y from normalized device coordinates to window
coordinates. Let ( xnd , ynd ) be normalized device coordinates. Then the window coordinates ( xw , yw )
are computed as follows:

xw = ( xnd + 1 )( width / 2 )
yw = ( ynd + 1)( height / 2 ) + y

Viewport width and height are silently clamped to a range that depends on the implementation. To query this range, call glGet with argument GL_MAX_VIEWPORT_DIMS.
````

***Error:***
````
GL_INVALID_VALUE is generated if either width or height
is negative.
````

***Version Support***

|                         | OpenGL Version     |
| :---------------------- | :----------------- |
| Function / Feature Name |                    |
