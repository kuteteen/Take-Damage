# Take-Damage
Take Damage hook hook made to increase weapon damage, the game I made is Free Fire in version 1.65

# Bool
bool isTakeDemageBool = false

# Hook
int (*Take_Damage)(void *instance);
int TakeDamage(void *instance) {
    if(instance != NULL) {
        if (isTakeDemageBool) {
           return 50; //Input the damage you want the weapon to deal
        }
    }
    return Take_Damage(instance);
}

# Offset
HOOK(0x8E4FCC, TakeDamage, Take_Damage);
