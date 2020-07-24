# Babel

## Function

Babel takes modern JS and compiles it down to useable JS code in old browsers which don't have new JS compatability. Use small babel plugins through npm to do this. A lot of new features need specific plugins for the feature to target. 

However, Babel also comes with presets which is like a package of plugins to fit certain application requirements, e.g: the last two versions of all the famous browsers. 

### Assistance

.babel rc is a file in your root folder that can be used to config your babel based production. People also sometimes do this same thing in package.json, and often use it with webpack