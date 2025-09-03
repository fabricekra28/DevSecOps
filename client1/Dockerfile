# Utiliser une image Node.js légère
FROM node:18-alpine

# Définir le répertoire de travail
WORKDIR /app

# Installer serve globalement pour servir les fichiers statiques
RUN npm install -g serve

# Copier les fichiers du frontend
COPY . .

# Variables d'environnement avec valeurs par défaut
ENV API_BASE_URL=http://localhost:5000/api
ENV APP_NAME="User Management System"
ENV NODE_ENV=production

# Exposer le port
EXPOSE 3000

# Commande pour démarrer l'application
CMD ["serve", "-s", ".", "-l", "3000"]
