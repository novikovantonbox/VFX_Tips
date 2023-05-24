# VEX Tips 
### VEX типы данных
```C#
float       f@name    // Floating point scalar values.
vector2     u@name    // Two floating point values. Could be used to store 2D positions.
vector3     v@name    // Three floating point values. Usually positions, directions, normals, UVW or colors.
vector4     p@name    // Four floating point values. Usually rotation quaternions, or color and alpha (RGBA).
int         i@name    // Integer values (VEX uses 32 bit integers).
matrix2     2@name    // Four floating point values representing a 2D rotation matrix.
matrix3     3@name    // Nine floating point values representing a 3D rotation matrix or 2D transform matrix.
matrix      4@name    // Sixteen floating point values representing a 3D transform matrix.
string      s@name    // A string of characters.
```
### VEX каналы
```C#
chf('flt2');            // Float
chi('int');             // Integer
chv('vecparm');         // Vector 3
chp('quat');            // Vector 4 / Quaternion
ch3('m3');              // 3x3 Matrix
ch4('m4');              // 4x4 Matrix
chs('str');             // String
chramp('r', x);         // Spline Ramp
vector(chramp('c', x)); // RGB Ramp
```
# Шпаргалки по Houdini
"/hip/Examples.hip" - тут лежат примеры описанные ниже. (Версия Houdini 19.0.720)
____
### Вращение векторов
/obj/Vector_Examples/vector_rotation<br/>
Вращение вектора `@up` по оси вектора `@N` на угол `angle`
```C#
float angle = chf('angle');
vector4 rot = quaternion(radians(angle), @N);
@up = qrotate(rot, @up); 
```
____
### Curve Boolean
https://www.toadstorm.com/blog/?p=529
____


