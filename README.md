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
            [
                'company' => 'LOHR - Sistemas Eletrônicos',
                'position' => 'Full-Stack Developer',
                'since_at' => '2024-07'
            ],
            [
                'company' => 'Plenatech - Excelência em TI',
                'position' => 'Web Developer',
                'since_at' => '2022-01',
                'exit_at' => '2024-07'
            ]
        ];
    }

    public function getFavoriteTechnologies () : array
    {
        return [
            Php::class,
            JavaScript::class,
            VueJS::class,
            TailwindCSS::class,
            Docker::class,
            Linux::class
        ];
    }
}
```
