# Tuppers_self-referential_formula
Emboding tupper's self-referential formula with python.

This time, I'll try the method how to embody 'tupper's self-referential formula'.
And to take it more invisible, I'll use '*'.
First of all, we should know the formula below;


$$
\frac{1}{2}< \lfloor mod(\lfloor \frac{y}{17}\rfloor 2^{-17 \lfloor x \rfloor - mod(\lfloor y \rfloor, 17) }, 2) \rfloor
$$

The formula is called 'tupper's self-referential formula' because when we draw the function, we will get the similar shape of the formula.
To change that formula into python code, you should set which text will be marker first.
As I noticed above, I'll use *, which is a marker.

The main structure is like below;
1. importing concept of 'floor'
2. defining function of the formula
3. assigning a proper value to a constant number 'k'
4. coding that drawing a function of tupper's self-referential formula

Then the code will appear like this;

    from math import floor
    def tuppers_formula(x, y):
      return 0.5< floor((y//17//2**(17*floor(x) + floor(y) % 17)) % 2)
    k = 960939379918958884971672962127852754715004339660129306651505519271702802395266424689642842174350718121267153782770623355993237280874144307891325963941337723487857735749823926629715517173716995165232890538221612403238855866184013235585136048828693337902491454229288667081096184496091705183454067827731551705405381627380967602565625016981482083418783163849115590225610003652351370343874461848378737238198224849863465033159410054974700593138339226497249461751545728366702369745461014655997933798537483143786841806593422227898388722980000748404719
    for y in range(k, k+17):
      for x in range(105, -1, -1):
        if tuppers_formula(x, y):
          print('*', end='')
        else:
          print(' ', end='')
      print('')

If you code like this, then result will be like this;
>>>
![튜퍼의 자기언급 공식](https://github.com/psjdavid/Tuppers_self-referential_formula/assets/94748252/3a4775d3-fba9-4af7-ba07-c3d239e08380)

We can find easily that it's a similar shape with the formula below!;

$$
\frac{1}{2}< \lfloor mod(\lfloor \frac{y}{17}\rfloor 2^{-17 \lfloor x \rfloor - mod(\lfloor y \rfloor, 17) }, 2) \rfloor
$$

This time, we became to know how to embody 'tupper's self-referential formula' with python.

*I'll inform that I'm inspired by 'ray_math' who is a Korean math youtuber.
Also, I referred WIKIPEDIA "Tupper's self-referential formula".
