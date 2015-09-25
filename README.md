# iOS-Framework-Crash
有些系统函数传入参数不对就会导致crash

1、传入参数为nil

[NSSet setWithObject:nil]
//[NSSet setWithObjects:nil]
[NSSet setByAddingObject:nil]

//[[NSMutableSet alloc] initWithObjects:nil]
[[NSMutableSet new] addObject:nil]
[[NSMutableSet new] removeObject:nil]

[[NSCountedSet new] addObject:nil]
[[NSCountedSet new] removeObject:nil]

[NSOrderedSet orderedSetWithObject:nil]
[[NSOrderedSet alloc] initWithObject:nil]

[[NSMutableOrderedSet alloc] initWithObject:nil]
[[NSMutableOrderedSet new] insertObject:nil atIndex:0]

[[NSMutableDictionary  new] setObject:nil forKey:nil]

[[NSMutableArray  new] addObject:nil]

[[NSAttributedString alloc] initWithString:nil]系列

...

2、index越界
NSString、NSMutableString
NSAttributedString、 NSMutableAttributedString
NSArray、NSMutableArray
...

objectAtIndex:
objectsAtIndexes:
setObject:atIndex:
replaceObjectAtIndex:withObject:
replaceObjectsAtIndexes:withObjects:
insertObject:atIndex:
insertObjects:atIndexes:
removeObjectAtIndex:
removeObjectsAtIndexes:
moveObjectsAtIndexes:toIndex:
exchangeObjectAtIndex:withObjectAtIndex:
exchangeSubviewAtIndex:withSubviewAtIndex:

[[NSMutableOrderedSet new] removeObjectAtIndex:1]

3、range越界
NSString、NSMutableString
NSAttributedString、 NSMutableAttributedString
NSArray、NSMutableArray

removeObject:inRange:

4、KVO的key值不正确
[NSObject valueForKey:]
[NSObject setValue:forKey:]
...

5、UIView
[one addSubView:one]
约束，Masonry
