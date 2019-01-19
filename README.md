# Java 9 Modules Intro

## Intial dir structure:
```
 λ ls -R
src    target

./src:
research.wayne.jpmshello

./src/research.wayne.jpmshello:
module-info.java research

./src/research.wayne.jpmshello/research:
wayne

./src/research.wayne.jpmshello/research/wayne:
jpmshello

./src/research.wayne.jpmshello/research/wayne/jpmshello:
HelloModules.java

./target:
```

## Compile
```
λ javac -d mods/research.wayne.jpmshello src/research.wayne.jpmshello/module-info.java src/research.wayne.jpmshello/research/wayne/jpmshello/HelloModules.java
```

### Compile Result
```
λ ls -R mods
research.wayne.jpmshello

mods/research.wayne.jpmshello:
com

mods/research.wayne.jpmshello/com:
mydeveloperplanet

mods/research.wayne.jpmshello/com/mydeveloperplanet:
jpmshello

mods/research.wayne.jpmshello/com/mydeveloperplanet/jpmshello:
```

## Execution
```
java --module-path mods --module research.wayne.jpmshello/research.wayne.jpmshello.HelloModules
```

### Execution Result
```
Hello Modules!
```