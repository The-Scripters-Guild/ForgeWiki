# Get Squad Definition From AI Spawner

Returns a squad definition from the *AI Spawner*, which contains unit and spawning data based off of the spawner's 
*Object Properties*. Optionally apply *Squad Overrides* before returning.

## Inputs
| Input            | Type             | Required | Description												    |
|------------------|------------------|----------|--------------------------------------------------------------|
| AI Spawner       | Object           | Yes      | The AI spawner object used to retrieve the squad definition. |
| Squad Overrides  | Squad Overrides  | No       | The squad overrides to apply to the squad definition.        |

## Outputs
| Output           | Type             | Description												            |
|------------------|------------------|-----------------------------------------------------------------------|
| Squad Definition | Squad Definition | The squad definition from the AI spawner with any overrides applied. |

**Contributors**

Mr. Admirals