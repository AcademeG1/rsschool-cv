## Michail Ignatovich
----------------------------------
## My Contacts

* Address: Yakub Kolos St. Minsk, Belarus
* Phone: +375333148439
* e-mail: m-ignatovich@hotmail.com
* GitHub: academeg1

----------------------------------- 

## Summary

I am currently studying at the university. I'm just starting my career path. At the same time I study FrontEnd in courses from RSSchool. My goal is to learn, to learn everything new and exciting. I like to write code and read books. I spend a lot of time doing my favorite things. My strong point is problem solving, perseverance and quick learning in various fields. I would like to gain knowledge and skills that will be enough for employment in the company and successful development in the future.

-------------------------------------

## My future skills

* HTML
* CSS(Framework Bootstrap, Preprocessor SCSS)
* JavaScript (Fundamentals,Functional Programming, OOP, Asynchronous JavaScript, ES6+,DOM)
* Version control: Git (service GitHub)

--------------------------------------

## My current skills

* C++ (basic knowledge) 
* Python(Fundamentals, OOP, Async) - Django Framework(basic knowledge)
* SQLite(basic knowledge)
* Windows OS, Linux(Ubuntu), Mac OS
* Figma
* Editors: Brackets, PyCharm, PhpShtorm, VSCode.

---------------------------------------

## Example of my Python code

```
class FSMAdmin(StatesGroup):
    photo = State()
    name = State()
    description = State()
    price = State()

async def cm_start(message : types.Message):
    await FSMAdmin.photo.set() 
    await message.reply('Загрузи фото')

# @dp.message_handler(commands=['photo'], state=FSMAdmin.photo)
async def load_photo(message : types.Message, state : FSMContext):
    async with state.proxy() as data:
        data['photo'] = message.photo[0].file_id
    await FSMAdmin.next()
    await message.reply('Теперь введи название для пиццы:')

# @dp.message_handler(state=FSMAdmin.name)
async def load_name(message : types.Message, state : FSMContext):
    async with state.proxy() as data:
        data['name'] = message.text
    await FSMAdmin.next()
```

--------------------------------------