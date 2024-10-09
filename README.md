```php
<?php

class DeveloperProfile {
    public readonly string $name;
    public readonly string $role;
    public readonly array $skills;

    public function __construct(
        string $name = "Ricardo",
        string $role = "PHP Backend Developer",
        array $skills = ["PHP", "Laravel", "API Development", "Backend Architecture", "SQL", "UNIX"]
    ) {
        $this->name = $name;
        $this->role = $role;
        $this->skills = $skills;
    }

    public function getProfile(): array {
        return [
            'Name' => $this->name,
            'Role' => $this->role,
            'Skills' => implode(", ", $this->skills)
        ];
    }
}

$me = new DeveloperProfile();

var_dump($me->getProfile());

?>
```
