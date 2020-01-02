# Python_Bootcamp
A training camp for Python learning


# function document
def MyFirstFunction(name):
    'name in function define is parameter.'
    # parameter is a form presenting position ocupy
    print("argument: " + name)

MyFirstFunction('cake')   # argument: cake

MyFirstFunction.__doc__   # 'name in function define is parameter.'
help(MyFirstFunction)
print.__doc__
help(print)

def AnimalDesc(name, habit):
    print(name + '->' + habit)

AnimalDesc('Cat', 'Catch mouses')   # Cat -> Catch mouses
AnimalDesc('Climb trees', 'Monkey')   # Climb trees -> Monkey
# 关键字参数 keyword parameter
AnimalDesc(habit='Eat bamboo', name='Panda')   # Panda -> Eat bamboo

# 默认值参数 default value parameter
def AnimalDesc2(name='Human', habit='Make tools'):
    print(name + '->' + habit)

AnimalDesc2()   # Human -> Make tools
AnimalDesc2('Indian')   # Indian -> Make tools
AnimalDesc2('Shark', 'Live in the sea')   # Shark -> Live in the sea

# 收集参数/可变参数
def test(*params):
    print('Length of parameters: ', len(params))
    print('The second parameter: ', params[1])

test(1, 'Ice cream', 2, 3)   # Length of parameters: 4, The second parameter: Ice cream

def test(*params, exp):
    print('Length of parameters: ', len(params), exp)
    print('The second parameter: ', params[1])

test(1, 'Ice cream' 2, 3, exp=666)   # Length of parameters: 4 666, The second parameter: Ice cream

def test(*params, exp=999):
    print('Length of parameters: ', len(params), exp)
    print('The second parameter: ', params[1])

test(1, 'Ice cream' 2, 3)   # Length of parameters: 4 999, The second parameter: Ice cream
