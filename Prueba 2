libros=["mago de oz","narnia","los viajes de gulliver","paco yunque"]
cantidad=[5,2,3,7]
Usuarios=["100000000"]
libros_sacados=["ninguno"]
cantidad_sacada=[0,]
def lol():
  print("inserte libro")
  t=str(input())
  if t!="acabe" and t not in libros:
    print("inserte cantidad existente")
    r=int(input())
    if r>=1:
      libros.append(t)
      cantidad.append(r)
    if r==0:
      lol()
  print(libros)
  print(cantidad)
  print(Usuarios)
  print(libros_sacados)
  return ""

def sacar_libros(ñ):   #variables utilizadas: i,r,t,s,cantS,a,b,c,d,e,f,g,h,j,k,l,m,ids,reg,ñ,n,o
  print("que libros desea sacar?(entre comas)")
  registro=""
  s=str(input())
  s=s.split(",")
  for j in range(len(s)):
    if s[j] not in libros:
      print("el libro",s[j],"no existe en la base de datos")
      s.remove(s[j])
  print(s)
  for k in range(len(s)):
    if k>=1:
      registro=registro+","+s[k]
    else:
      registro=registro+s[k]
    print("inserte la cantidad de ejemplares a sacar de libro",s[k],":")
    cantS=int(input())
    a=libros.index(s[k])
    if cantS>=1 and cantidad[a]-cantS>=0:
      b=cantidad[a]-cantS
      cantidad.insert(a,b)
      cantidad.pop(a+1)
    else:
      print("No se tiene cantidad deseada. Solo quedan:",cantidad[a],"libros")
  print(ñ)
  n=Usuarios.index(ñ)
  if registro!="":
    libros_sacados.insert(n,registro)
    libros_sacados.pop(n+1)
  print(registro)
  print(libros)
  print(cantidad)
  print(Usuarios)
  print(libros_sacados)
  return ""

def devolver_libros():
  print("que libros desea devolver?(entre comas)")
  d=str(input())
  d=d.split(",")
  for c in range(len(d)):
    if d[c] not in libros:
      print("el libro",d[c],"no ha sido sacado de la base de  datos")
      d.remove(d[c])
  print(d)
  for g in range(len(d)):
    print("inserte la cantidad de ejemplares a devolver de libro",d[g],":")
    e=int(input())
    h=libros.index(d[g])
    cantidad.insert(h,cantidad[h]+e)
    print(cantidad[h])
    cantidad.pop(h+1)
  print(libros)
  print(cantidad)
  return ""

def registrar_usuario():
  #variables utilizadas: i,r,t,s,cantS,a,b,c,d,e,f,g,h,j,k,l,m,ids
  print("tiene usuario? (si/no)")
  m=str(input())
  if m=="no":
    print("le crearemos un id")
    l=int(Usuarios[len(Usuarios)-1])+1
    Usuarios.append(str(l))
    print("su id es",l)
  print("inserte su usuario")
  ids=str(input())
  if ids in Usuarios:
    return ids
  else:
    print("su usuario no esta registrado o no tiene")
    registrar_usuario()
  return ids
  
def registro_usuario(n):
  pass

for i in range(2):
  while i>=0:
    print("(1)añadir a base de datos/(2)sacar/(3)poner libros")
    f=int(input())
    if f==1:
      lol()
    if f==2 or f==3:
      reg=registrar_usuario()
      if f==2:
        sacar_libros(reg)
      if f==3:
        devolver_libros()
