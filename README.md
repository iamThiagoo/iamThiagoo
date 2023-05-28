```php
<?php

namespace Thiago\Ferreira;

class About extends Me
{
    public function User () : User
    {
        $myUser = User::updateOrCreate([
            'name' => 'Thiago Ferreira'
        ], [
            'age' => 19,
            'country' => 'Brazil',
            'social_gmail' => 'devthiagoferreira@gmail.com',
            'social_linkedin' => 'https://www.linkedin.com/in/imthiagoferreira/'
        ]);
        
        return $myUser;
    }

    public function Experiences () : array
    {
        return [
            'workplace' => [
                'company' => 'Plenatech',
                'position' => 'Web Developer',
                'since_at' => '2022-01-17 00:00:00'
            ]
        ];
    }

    public function FavoriteTechnologies () : array
    {
        return [
            Laravel::class,
            PHP::class,
            JavaScript::class,
            TailwindCSS::class,
            Docker::class,
            Linux::class,
            VSCode::class
        ];
    }
}
```
