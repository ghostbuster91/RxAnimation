# RxAnimation
This is Animation wrapping Observable.
You can get event Observable.
And you can call animation chain more simple.

## Offer
- rx-animation
- rx-animation-kotlin

## Classes
- RxAnimation
- AnimationEvent
- AnimationEventOnSubscribe

## Example

```Java
Animation animation = new ScaleAnimation(0.0f, 0.0f, 1.0f, 1.0f);
RxAnimation.events(animation)
    .subscribe(new Subscriber<AnimationEvent>() {
        @Override
        public void onCompleted() {
               
        }
    
        @Override
        public void onError(Throwable e) {
            
        }
    
        @Override
        public void onNext(AnimationEvent animationEvent) {
            switch (animationEvent.kind()) {
                case START:
                    break;
                case REPEAT:
                    break;
                case END:
                    break;
            }
        }
    });
```