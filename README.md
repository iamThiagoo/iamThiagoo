```php
<?php

namespace Thiago\Ferreira;

class About extends Me
{
    public function getUser () : User
    {
        $user = App\Models\User::updateOrCreate([
            'name' => 'Thiago Ferreira'
        ], [
            'age' => 20,
            'country' => 'Brazil',
            'social_gmail' => 'devthiagoferreira@gmail.com',
            'social_linkedin' => 'https://www.linkedin.com/in/imthiagoferreira/'
        ]);
        
        return $user;
    }

    public function getExperiences () : array
    {
        return [
            'workplace' => [
                'company' => 'Plenatech',
                'position' => 'Web Developer',
                'since_at' => '2022-01-17'
            ]
        ];
    }

    public function getFavoriteTechnologies () : array
    {
        return [
            Laravel::class,
            Php::class,
            JavaScript::class,
            TailwindCSS::class,
            Docker::class,
            Linux::class,
            VSCode::class
        ];
    }
}
```
