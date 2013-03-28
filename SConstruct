prod_env= Environment(LIBS=['pthread'],
CCFLAGS=["-W","-Wall","-Werror","-O2"],
CC='gcc')
debug_env= Environment(CCFLAGS=["-g","-ggdb3","-W","-Wall","-Werror"],
LIBS=['pthread'],
CC='gcc')

env = prod_env
if 'debug' in ARGUMENTS:
	env = debug_env

env.Program('httpstub',['httpstub.c'])


