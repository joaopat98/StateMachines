# Unity-StateMachines

This Unity package contains core classes intended to be used for the creation of entities that implement a state-machine pattern in Unity Projects. This can be useful for the creation of enemies and other NPCs.

## Usage

To create a behaviour that implements the state-machine pattern, it should inherit from the StateMachineBehaviour class. This is not necessary, but this class already has some base functions and members that facilitate this implementation. An example of such an implementation can be found in [PingPong.cs](Assets/StateMachines/Examples/PingPong/PingPong.cs), shown below:

```csharp
public class PingPong : StateMachineBehaviour<PingPong>
{
    public float TimeBetweenStates;

    protected override void Start()
    {
        state = PingState.Create(this);
    }
}
```

https://github.com/joaopat98/Unity-StateMachines/blob/b30b40601ea8b2d89c29a307add949030d8b947a/Assets/StateMachines/Examples/PingPong/PingPong.cs#L3-L11